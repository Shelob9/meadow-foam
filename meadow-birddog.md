# BirdDog

Problems

- People want to write long tweets
  - Twitter alt tags can hold a ton more text then tweets
- Text without decoration is boring.
  - One thing I miss about Facebook is ability to decorate words with colors and shape a litte.
- People often use screenshots of notes app or highlights from articles.
  - Solves problem, but this makes the text unreadbale with a screen reader.
- Sharing large chunks of article with a screenshot also a common solution
  - Can be clunky looking, requires editting.
  - Not accessible.

## Solution

Chrome Extension that lets you write a bunch of text, then send a tweet with image(s) of text.

Laravel application for backend.

### Uses

- Write a long tweet.
- Share article screenshot with alt text.
  - screenshot tool.
- Make long tweet look cool with fonts and background colors.
- Mutli-panel comics. Upload art and text. Look good, be accessible, all death engine friendly.
- Author with Gutenberg block.
  - Create from a share block -- Add-on for Ben's plugin.
  - Create from that cool cover block.

### Extension

- Context menu item for share accessible.
  - Opens in option page.
- Option page has
  - Auth
  - tweet editor
- Could just redirect to app on share.

### application

- Auth
- Possible eCommerce
- Tweet editor
- Tweet scheduler/poster
  - Borrow or abstract TwitterService from Meadow, which already has it
