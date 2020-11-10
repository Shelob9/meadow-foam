# Growing Into Graphs and Gardens

> [Memory systems make memory into a choice, rather than an event left up to chance: This changes the relationship to what we’re learning, reduces worry, and frees up attention to focus on other kinds of learning, including conceptual, problem-solving, and creative.](https://numinous.productions/ttft/#summary)
 >   - [Andy Matuschak](https://andymatuschak.org),[Michael Nielsen](http://michaelnielsen.org)

When I get asked what I do for a living, if I'm not being snarky, I say "I make tools for people who make websites." Since I've mainly made WordPress plugins and tools for people who make WordPress plugins and similar, that's pretty accurate.

I've always been more interested in how things work then using them as they are intended to work. Beacuse I was labelled as learning disabled as kid, I was forced to translate how I think and write into neurotypical.

When I discovered HTML as a kid, a big part of why I was so excited and fasinated by was beacuse it was extensible and universal. It could be made to work for different types of people. When I discovered I could play with open source content managment systems (CMS) like WordPress and Wikipedia, I felt the same way.

This bubble is about different types of CMS, how they are evolving to be more graph-like and why that's good if personal puiblishing is trending more towards [[digital-gardens]].

## Useful Generalizations About CMSes

Traditionally, we categorize "website building software" into two genres -- blog/ page builder and wikis. Examples of the blogs/ page builder model -- Geocities, Squarespace, Shopify and [[WordPress]]. The best example of the second category is Wikipedia. Yes, Wikipedia is not the only implimentation of Wikimedia's software, which isn't the only Wiki software, but I'm going to generalize for a bit.

 Blogs and page builds make authorship visible. It's generally clear on a database and presentation level who is __the__ author of the content. These types of CMSes have implicit, intentionally defined relationships between content. This is acchived with tagging, categorization and other types of assocation that can be stored with a relational database.

  In the second category, wikis, authorship is collective and relationships between content emerge through bi-directional linking. WordPress and similar site builders may have discussion as a feature in comments or forums, but it's general clear who wrote what.
  
  Wikipedia uses a lot of [transclusion](https://en.wikipedia.org/wiki/Help:Transclusion) a feature that allows content to be embeded transperantly in multiple locations.

  In contrast to transclusion, blogs and page builders tend to make the boundries between a post or page's content and embeded sources obvious. Embeded tweets, YouTube videos or even use of the HTML blockquote tag are generally styled a part from the content. It is common that embeded content is loaded by the browser in an iFrame, which sandboxes that content from the rest of the page.

## Optimizing For Thaught Work

Not only are these generalizations way too general. They are also dated. Content managment systems are evolving to be more graph-based. Graph databases and visual concepts are better equipped to query and represent data for thaught work.

This shift is a gradient in difference from traditional relational databases and object-oriented programming to graph databases and functional/ state-machine programming.

### What About Roam or Twitter?

Social networks don't fit into this categorization. Neither does Roam or [[Foam]], sort of. Roam is a single author knowledge graph with wiki-style links that structure emerges from. It's both really. Roam is a working on multiplayer. That and the #RoamCult ecosystem make it into more of a network.

WordPress -- WordPress.com and the open source ecosystem -- don't really fit that distinction either. Sites are optionally federated using Jetpack. Reusable blocks add wiki-style transclusion a default feature of the software.

## Everything Is A Graph Anyway

> [Your work, no matter what you do, will take time. If you know what your goals are, you can start the process now and patiently guide it to where it needs to go. Give them space to grow, or create space later. In order to flourish, you need to allow room to move into. Or, prepare a move once they’ve outgrown the space you planned. Track what matters and do something with it](https://josepha.blog/2020/09/09/gardens-are-just-zoos-for-plants-my-sabbatical-in-the-garden/)

I spend a lot of time thinking about the wisdom of trees and the small plants around me. They grow in intelligent ways. Turning towards the sun. I tend to a decent amount of house plants -- I've had that kind of pandemic -- and they are great reminders that good design isn't about control, it's about what possibilities you create or make less probable. Also the danger of drastic action.

There are a lot of complex relationships in growing plants. A lot of energy comes from the sun, that's important. So is getting nutrients and moisture from the soil.

At one point in my life -- I went to school for environmental studies -- I understood how to diagram those flows. By doing so a graph of the relationships in the system emerges.

Today, I understand my plants on a less detailed level. I do have a white board that I'm always using to diagram a process or work out my thaughts on something.

Whenever we organize our thaughts -- in conversation, in words, etc -- there is a graph of the relationships between the concept. Whether we make the graph or not, it's there. Graphs of relationships are an emergent property of content creation and human conversation.

Technologies like Roam, Git or GrpahQL or graph databases allow us to design communication systems with the understanding that we are creating a graph. I belive that makes them better equipped for the tools of thaught work.

## Purpose Is Emergent

> [Luhmann, the godfather of the Zettelkasten Method himself, wrote that it is not important where you store a Zettel as long as you can reference it from every other point to the Zettelkasten](https://zettelkasten.de/posts/luhmann-folgezettel-truth/)

Wikis have no implied structure. The possiblity of content is created by the use of a bi-directional link to it. The graph of the bi-directional links between content is often a meaningful structure. It is not an intentional structure like a book or an essay.

 Wikis are great tools for collecting knowledge, that there is a broad consensus on. The most useful wiki is Wikipedia -- an encylopedia of common facts and figures. Great stuff.

Using wikis for multi-author, pseudonymous work on highly subjective content isn't super common.  

### Digital Gardens

> [The possibility to create a direct reference, for example as a link, reduces the importance of the Zettel coming next in the sequence. The technique Folgezettel creates value from the position of a Zettel in the archive. But the technique of creating a link reduces the value of the position of a Zettel.
>
> Looks like a paradox, doesn’t it?
>
> But Luhmann gave us a technique to handle these. He called it “unfolding a paradox”.2 You take a step back and make another distinction.](https://zettelkasten.de/posts/luhmann-folgezettel-truth/)

[[digital-gardens]] seam to be single player, for the most part. But, many are hosted on Github, so anyone can suggest an edit. I love the idea of git-based content creation. It's not open edit, but it's open to editting. It doesn't erase authorship, but it obscures it.

Also, digital gardens can be database-driven. A Roam database, for example could be used and Roam is becoming mutli-player.

### Oppurtunities To Improve Digital Garden Ecosystem

> [Memory systems are in their infancy: it is possible to increase effective human memory by an order of magnitude, even beyond what existing memory systems do; and systems such as the mnemonic medium may help expand the range of subjects users can comprehend at all.](https://numinous.productions/ttft/#summary)
 >   - [Andy Matuschak](https://andymatuschak.org),[Michael Nielsen](http://michaelnielsen.org)
 
Digital gardens as the thing you own, you tend, you decide who can join you in tending. That's awesome, but what concerns me is I spent years hearing WordPress people talk about the value -- to end users -- of "owning your own content" and then tons of bloggers went to Medium for the network effects.

I belive that digital gardens, including private or members only digitial gardens could be the place where content is created and syndicated from. For example, I could write a [dev.to](https://dev.to) or Medium API integration to publish a completed bubble.

Both platforms support cannonical linking to the original source of the article. This would allow me to benefit from the audience size and recomendation alogrithms on those platforms. If you've read this far and it's not obvious that I'm sort of building all of this in my spare time, yes I am.

Having limited access or membership-based digital garden sites would also allow for gardeners to monetizate there content. Generating PDFs -- call it an eBook if you're a marketter -- from content is another oppurtunity to engage in capitalism.

Right now, making these sites requires some web development skills. Understanding the npm command line inteface should not be a requirment for setting up a digital garden. A no-code digital garden builder would be super cool.

Also, more educational resource about how to use availble open source tools to build/ maintain digital gardens would be great. See: [[digital-gardens]] for some help.

 Proposals such as [open transclude](https://subpixel.space/entries/open-transclude/) are a great way for content to live in multiple gardens. I belive there is a lot more room for growth here. Specifically I belive that multi-player knowledge graph creation and publishing is evolving very quickly and in interesting ways. That's super cool and I am excited to see what happens.

 As someone who has spent a ton of time in working in the WordPress space, I am  fasinated by the opprtunity for inovation in digital publishing that digital garden-grown content creates. How do we take this content and make it more availble, discoverable and potentially monetizable so that the system is sustaninable? That's the part I am interested in building.

[[meadow-birddog]]

[//begin]: # "Autogenerated link references for markdown compatibility"
[digital-gardens]: digital-gardens "Digital garden"
[meadow-birddog]: meadow-birddog "BirdDog"
[//end]: # "Autogenerated link references"