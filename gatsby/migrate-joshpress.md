
Immediate goal: Get JoshPress.net off of WordPress and into a static site. Either as an archive or the starting point for new Gatsby-powered blog.


## Overengineering Version One

@todo

## Overengineering Version Two

If i wanted to keep WordPress site, I probably would have done it [this way](https://justinwhall.com/headless-wordpress-gatsby-netlify-continous-deployment/).

* Install Yoast meta - https://wordpress.org/plugins/wp-rest-yoast-meta/
* Create blog 
    * Use Gatsby Starter Blog
    * `yarn add gatsby-source-wordpress`
    * Add WordPress options to gatsby-config https://www.gatsbyjs.org/packages/gatsby-source-wordpress/
* Shadow gatsby-node.js
    * https://stackoverflow.com/questions/58225214/how-can-i-override-the-createpages-query-from-a-gatsby-theme
* Rebuild site
* Checkout WordPress Data Availble Via GraphQl

Click the "wordpressPoss" query and create a query for one post:
```graphql
query MyQuery {
  wordpressPost{
    title,
    excerpt
    date
  }
}
```

Many posts:
```graphql
query MyQuery {
  allWordpressPost(limit: 10) {
    nodes {
      link
      title
    }
  }
}
```

Next pages's data with edges:
```
query MyQuery {
  allWordpressPost(limit: 10) {
    nodes {
      title
      link    
    },
    edges {
      next {
        link,
        title
      }
    }
  }
}
```

Featured Image Data:

```
query MyQuery {
  allWordpressPost(limit: 10) {
    nodes {
      title
      link
      featured_media {
        localFile {
          url,
          publicURL,
          absolutePath,
          relativePath
        }
        alt_text
      }
    },
    edges {
      next {
        link,
        title
      }
    }
  }
}
```

Add images for eeels:
https://www.gatsbyjs.org/tutorial/wordpress-image-tutorial/

* yarn add gatsby-plugin-sharp
* yarn add gatsby-transformer-sharp
gatsby-remark-images gatsby-plugin-sharp

Then I did a rebuild and got error `The plugin "default-site-plugin" created a node of a type owned by another plugin.

## Three
Start from matson's starter repo

```jsx
const FeaturedImage = ({node}) => {
	if( ! node.featuredImage ){
		return <React.Fragment />
	}
	const {featuredImage} = node;
	return <img src={featuredImage.sourceUrl} alt={featuredImage.altText} />

}

```

cahnge Page Query
```javascript
export const pageQuery = graphql`
	query {
		wpgraphql {
			posts {
				edges {
					node {
						id
						postId
						slug
						status
						categories {
							edges {
								node {
									categoryId
									name
									slug
									link
								}
							}
						}
						title
						content
						date
						author {
							name
							slug
						}
						featuredImage {
							altText
							sourceUrl
							caption
							title
						}
					}
				}
			}
		}
	}
`;
```

Install imgage plugins
* yarn add gatsby-transformer-sharp gatsby-remark-images gatsby-plugin-sharp