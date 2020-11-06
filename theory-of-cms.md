# Theory of Content Management Systems

>[Memory systems make memory into a choice, rather than an event left up to chance: This changes the relationship to what we’re learning, reduces worry, and frees up attention to focus on other kinds of learning, including conceptual, problem-solving, and creative.](https://numinous.productions/ttft/#summary)
  - [Andy Matuschak](https://andymatuschak.org),[Michael Nielsen](http://michaelnielsen.org)

Hypothesis: Content managment systems are evolving to be more graph-based. This statment applies to conceptual models, and user experience as well as to database and software development patterns.

This shift is a gradient in difference from traditional relational databases and object-oriented programming to graph databases and functional/ state-machine programming.

Traditionally, we have two models -- blog/ page builder and wikis. In the blogs/ page builder category -- Geocities, Squarespace, Shopify [[WordPress]] -- you have flexible model where authorship is visible and relationships between content is defined implicitly through tagging. In the second category -- Wikipedia being the archetype, but not only implimentation of Wikimedia's software, which isn't the only Wiki software -- authorship is collective and relationships between content emerge through linking.

## Make Some Hyper-Generalized Distinctions

WordPress and similar CMSes:

- Clarifies authorship
  - Makes creation a singular act.
- Defines visible bounderies around embeds.
  - oEmbeds
  - iFrames
  - Blockquotes in HTML.
- Mutli-author via multiple identities
  - Discussion via forum/ comments
  - Multi-author blogs

Wikipedia

- Obscures authorship
  - Makes creation collective
- Obscures embeds
  - Transclusion
- Encourages open collaboration and editting
  - Defaulys to open editting.

## What About Roam or Twitter?

Social networks don't fit into this categorization. Neither does Roam or [[Foam]], sort of. Roam is a single author knowledge graph with wiki-style links that structure emerges from. It's both really. Roam is a working on multiplayer. That and the #RoamCult ecosystem make it into more of a network.

WordPress -- WordPress.com and the open source ecosystem -- don't really fit that distinction either. Sites are optionally federated using Jetpack. Reusable blocks add wiki-style transclusion a default feature of the software.

## Everything Is A Graph Anyway

> [Your work, no matter what you do, will take time. If you know what your goals are, you can start the process now and patiently guide it to where it needs to go. Give them space to grow, or create space later. In order to flourish, you need to allow room to move into. Or, prepare a move once they’ve outgrown the space you planned. Track what matters and do something with it](https://josepha.blog/2020/09/09/gardens-are-just-zoos-for-plants-my-sabbatical-in-the-garden/)

I spend a lot of time thinking about the wisdom of trees and the small plants around me. They grow in intelligent ways. Turning towards the sun. I tend to a decent amount of house plants -- I've had that kind of pandemic -- and they are great reminders that good design isn't about control, it's about what possibilities you create or make less probable. Also the danger of drastic action.

Graphs of relationships are an emergent property of content creation and human conversation. Technologies like Roam, Git or GrpahQL or graph databases allow us to design communication systems with the understanding that we are creating a graph.

## Purpose
> [Luhmann, the godfather of the Zettelkasten Method himself, wrote that it is not important where you store a Zettel as long as you can reference it from every other point to the Zettelkasten](https://zettelkasten.de/posts/luhmann-folgezettel-truth/)

Wikis have no implied structure. The possiblity of content is created by the use of a bi-directional link to it. The graph of the bi-directional links between content is often a meaningful structure. It is not an intentional structure like a book or an essay.

 Wikis are great tools for collecting knowledge, that there is a broad consensus on. The most useful wiki is Wikipedia -- an encylopedia of common facts and figures. Great stuff.

Using wikis for multi-author, pseudonymous work on highly subjective content isn't super common.  

## Digital Gardens

> [The possibility to create a direct reference, for example as a link, reduces the importance of the Zettel coming next in the sequence. The technique Folgezettel creates value from the position of a Zettel in the archive. But the technique of creating a link reduces the value of the position of a Zettel.
>
> Looks like a paradox, doesn’t it?
>
> But Luhmann gave us a technique to handle these. He called it “unfolding a paradox”.2 You take a step back and make another distinction.](https://zettelkasten.de/posts/luhmann-folgezettel-truth/)

[[digital-gardens]] seam to be single player to be single player. But, many are hosted on Github, so anyone can suggest an edit. I love the idea of git-based content creation. It's not open edit, but it's open to editting. It doesn't erase authorship, but it obscures it.

Also, digital gardens can be database-driven. A Roam database, for example could be used and Roam is becoming mutli-player. Also, like I'm building [[meadow]] with a relational database -- using [[laravel.md]], and [[meadow-halloween]] with that database and git-backed CMS. --Josh, start using a lot more words, so you make sense. Less concepts per square inch please --

Digital gardens as the thing you own, you tend, you decide who can join you in tending is a great evolution of this trend. To make them more useful and availble:

- More understanding of how to use availble open source tools to build/ maintain these tools.
- Nocode builders
- Multi-player.



> [Memory systems are in their infancy: it is possible to increase effective human memory by an order of magnitude, even beyond what existing memory systems do; and systems such as the mnemonic medium may help expand the range of subjects users can comprehend at all.](https://numinous.productions/ttft/#summary)
 >   - [Andy Matuschak](https://andymatuschak.org),[Michael Nielsen](http://michaelnielsen.org)

 Proposals such as [open transclude](https://subpixel.space/entries/open-transclude/) are a great way for content to live in multiple gardens. I belive there is a lot more room for growth here. Specifically I belive that multi-player knowledge graph creation and publishing is evolving very quickly and in interesting ways. That's super cool and I am excited to see what happens.
 
 As someone who has spent a ton of time in working in the WordPress space, I am  fasinated by the opprtunity for inovation in digital publishing that digital garden-grown content creates. How do we take this content and make it more availble, discoverable and potentially monetizable so that the system is sustaninable? That's the part I am interested in building.

[[meadow-birddog]]

## More Words About Graphs

Graphs aremore useful tool for representing reality beacuse they show how much the estiamte fits. Right and wrong is subjective. I am intrested in a gradient between total bullshit and fairly useful algorithm for predicting future events and analyzing past event.

This is the difference between meta graphs and intentional graphs. Meta graphs are emergent, intentional grpahs are not, but meta graphs do emerge between them.

[//begin]: # "Autogenerated link references for markdown compatibility"
[digital-gardens]: digital-gardens "Digital garden"
[meadow]: meadow "Meadow"
[laravel.md]: laravel "Laravel"
[meadow-halloween]: meadow-halloween "Meadow (Halloween)"
[meadow-birddog]: meadow-birddog "BirdDog"
[//end]: # "Autogenerated link references"