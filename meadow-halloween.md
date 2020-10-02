# Meadow (Halloween)

I am working on networked-mind tool called [[meadow]] at a very leisurly pace. My goal is to build a collaborative publishing tool. My first step is to build something that can display my blog posts, which are all on different sites, my clippings, my notes, as well as content from social media. I called the step "Halloween" beacuse I love the song Halloween by Mastodon. Also, I wish there was more times of the year where we reminded ourselves that we can be whoever we want to be.

## Content Types

### Clippings

These are quotes and hyperlinks I gathered using the Meadow PWA. This content is currently stored in a MySQL database. I used [[Laravel]] to build a REST API for clippings. The Laravel app also serves a basic PWA. This allows me use the native "Share" feature on my phone to add clippings.

### Posts

These are blog posts I have written on dev.to and on various WordPress sites. The WordPress posts are pulled into the site using The WordPress REST API.

### Bubbles

These are in progress notes. I write these using VSCode using [Foam](https://foambubble.github.io/foam/) a personal knowledge management and sharing system inspired by [Roam Research](https://roamresearch.com/). I built a [[markdown-api]] to get the content from Github, into this site.

## How Halloween Works

> [Source](https://github.com/shelob9/meadow-halloween)
>
> [URL](https://garden.joshpress.net).

Halloween uses [[next]] for the front-end client and additional API routes. I used [[tailwind]] css. There is a login page that allows login using Githun -- it only works if you authenticate as me, for now. The auth system was built using the most excellent [Next Auth](https://github.com/nextauthjs/next-auth).

## Next Steps

- Simplify and standardize UI
- Embeded Bubble editor
  - Markdown
  - Run Foam janitor on bubbles -- in API before save or Github action after commit?
  - Bubble graph.
  - Content PR submissions
  - Contributor visualization
- Graph of relationships between contents.
- For logged in user, Twitter timeline and favorites with clip button
- Button to create a PR to edit a bubble.
- Button to fork a bubble into your own bubble.


