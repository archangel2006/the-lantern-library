# The Lantern Library

A collection of 17 illustrated picture stories, each nine pages long, with a landing page that works like a small online library. Everything is plain HTML, CSS and a little JavaScript. There is no build step, no framework and no images to download, because every illustration is drawn in inline SVG.

## What's in the folder

```
storybook-library/
├── index.html          The landing page (loading screen, book covers, filters)
├── README.md           This file
└── stories/
    ├── tide-storybook.html
    ├── fox-echoes-storybook.html
    └── ... 15 more story files
```

## How to open it

1. Unzip the folder.
2. Open `index.html` in any modern browser.
3. Click a book cover to read that story. Every story has a "← Library" button in the top-left corner that brings you back.

To put it online, upload the whole `storybook-library` folder to any static host (Netlify, GitHub Pages, Vercel, a plain web server). Keep `index.html` and the `stories` folder side by side so the links keep working.

## The stories

| # | Title | Mood | Notes |
|---|-------|------|-------|
| 01 | The Night the Tide Got Lost | Cozy, Adventure | |
| 02 | The Fox Who Kept Echoes | Cozy, Adventure | |
| 03 | Pocket Waters the Moon | Cozy | Sequel is 04 |
| 04 | Pocket and the Star Garden | Cozy | Sequel to 03 |
| 05 | Gus Has the Hiccups | Funny | Sequel is 06 |
| 06 | Gus and the Birthday Cake Disaster | Funny | Sequel to 05 |
| 07 | Hugo Delivers the Mail | Cozy | Sequel is 08 |
| 08 | Hugo Gets a Letter | Cozy | Sequel to 07 |
| 09 | Wilbur Is Afraid of the Dark | Gently spooky, Cozy | Sequel is 10 |
| 10 | Wilbur and Theo Explore the Attic | Gently spooky, Cozy | Sequel to 09 |
| 11 | The Great Sandwich Mystery | Funny | Sequel is 12 |
| 12 | The Cheese Wheel Express | Adventure, Funny | Sequel to 11 |
| 13 | Biscuit and the Lost Star | Adventure | |
| 14 | Nell and the Great Indoor Expedition | Cozy, Adventure | |
| 15 | The Dragon Who Couldn't Roar | Funny, Adventure | |
| 16 | Marnie and the Midnight Market | Cozy, Adventure | |
| 17 | The Smallest Snowman | Cozy | |

Stories with a sequel are best read in order. Each sequel sits on the shelf right after the story it follows.

## Features

**Landing page**
- A loading screen with a swaying lantern, shown once per browser session.
- Illustrated book covers with a colour and picture for each story.
- Filter buttons for Cozy, Funny, Adventure, Gently spooky and Sequels.
- A "Surprise me" button that opens a random story.
- A "Stories that belong together" section listing the five stories that have a sequel.

**Stories**
- Each story has a cover and eight story pages, with the picture on one side and the text on the other.
- Pages scroll and snap into place, one page at a time.
- Gentle animations such as floating, twinkling and flickering, which switch off when the device asks for reduced motion.
- Automatic light and dark colour schemes.

## How it behaves on different screens

- **Desktop and wide screens:** the picture is on one side and the story text on the other, like an open book.
- **Phones and small tablets held upright:** each page is split into two full screens. The first shows only the illustration, edge to edge. The second shows only the story text, in a larger size.
- **Phones held sideways and short windows:** the picture and text stay side by side with tighter spacing and smaller text.

The picture screen on small devices stretches the sky of each scene upward to fill the screen, so nothing gets cropped.

## Adding a new story

1. Copy any file in `stories/` and rename it, for example `my-story-storybook.html`.
2. Replace the title, the text in each `<div class="card">`, and the SVG artwork in each `<div class="art">`.
3. In `index.html`, copy one of the `<a class="book" ...>` cards, change the `href` to `stories/my-story-storybook.html`, and update the title, tags and cover artwork.
4. Add the "← Library" button by copying the `<style>` block and the `<a class="lib-back">` link that sit right after `<body>` in any other story file.

Tags on a card (`data-tags="cozy adventure"`) control which filter buttons show it. The tags in use are `cozy`, `funny`, `adventure`, `spooky` and `sequel`.

## Technical notes

- **Fonts** are loaded from Google Fonts, so they need an internet connection. Without one, the pages fall back to your system fonts and still work.
- **Links:** each card in `index.html` has an `href` to a local story file and a `data-online` attribute. The `data-online` links are only used when the page is viewed inside Claude's preview, where it points to the hosted versions. On your own computer or host they are ignored.
- **Storage:** the loading screen uses `sessionStorage` to remember it has already played. If storage is unavailable, the page still works.
- **Browser support:** current versions of Chrome, Edge, Firefox and Safari.

## Credits

Written and illustrated with Claude, by Anthropic. All stories, characters and artwork are original.
