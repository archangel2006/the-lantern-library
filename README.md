
# 🏮 The Lantern Library
 
*A little library of picture stories, for bedtime, rainy afternoons and the hours in between.*
 
![Picture stories](https://img.shields.io/badge/picture-stories-hotpink?style=flat&labelColor=midnightblue)
![Bedtime approved](https://img.shields.io/badge/bedtime-approved-orange?style=flat&labelColor=midnightblue)
![Pure HTML CSS SVG](https://img.shields.io/badge/made_with-HTML_CSS_SVG-mediumaquamarine?style=flat&labelColor=midnightblue)
![No build step](https://img.shields.io/badge/build_step-none-cornflowerblue?style=flat&labelColor=midnightblue)
![Responsive](https://img.shields.io/badge/works_on-every_screen-mediumpurple?style=flat&labelColor=midnightblue)
![Dark mode](https://img.shields.io/badge/dark_mode-yes-slategray?style=flat&labelColor=midnightblue)
![Gentle motion](https://img.shields.io/badge/reduced_motion-respected-orchid?style=flat&labelColor=midnightblue)
![Made with Claude](https://img.shields.io/badge/made_with-Claude-coral?style=flat&labelColor=midnightblue)
 
</div>

## ✨ Once upon a time
 
There was a library with no walls and a single lantern. Inside lived tides that got lost, foxes who kept echoes in jars, a ghost who was afraid of the dark, and a dragon who could only squeak.
 
Every story is a picture book you scroll through, page by page. The pictures are drawn entirely in code, so there is nothing to download, nothing to install, and nothing to build. Open the lantern, pick a cover, and begin.
 
## 📖 Opening the book
 
- Open `index.html` in any modern browser.
- Click a cover to start reading. Every story has a small **Library** button in the corner that carries you back to the shelves.
Want to share it with the world? Drop the whole folder onto any static host, such as Netlify, GitHub Pages or Vercel, and keep `index.html` and the `stories` folder side by side so the paths stay happy.
 
```
storybook-library/
├── index.html      the landing page: lantern loading screen, covers, filters
├── README.md       you are here
└── stories/        every picture book, one file each
```


## 🕯️ On the shelves

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

## 🧭 Features

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

## 📚 Turning the pages; How it behaves on different screens

- **Desktop and wide screens:** the picture is on one side and the story text on the other, like an open book.
- **Phones and small tablets held upright:** each page is split into two full screens. The first shows only the illustration, edge to edge. The second shows only the story text, in a larger size.
- **Phones held sideways and short windows:** the picture and text stay side by side with tighter spacing and smaller text.

The picture screen on small devices stretches the sky of each scene upward to fill the screen, so nothing gets cropped.

## ## 🖋️ Writing a new tale

1. Copy any file in `stories/` and rename it, for example `my-story-storybook.html`.
2. Replace the title, the text in each `<div class="card">`, and the SVG artwork in each `<div class="art">`.
3. In `index.html`, copy one of the `<a class="book" ...>` cards, change the `href` to `stories/my-story-storybook.html`, and update the title, tags and cover artwork.
4. Add the "← Library" button by copying the `<style>` block and the `<a class="lib-back">` link that sit right after `<body>` in any other story file.

Tags on a card (`data-tags="cozy adventure"`) control which filter buttons show it. The tags in use are `cozy`, `funny`, `adventure`, `spooky` and `sequel`.

## 🔧 Behind the curtain; Technical notes

- **Fonts** are loaded from Google Fonts, so they need an internet connection. Without one, the pages fall back to your system fonts and still work.
- **Links:** each card in `index.html` has an `href` to a local story file and a `data-online` attribute. The `data-online` links are only used when the page is viewed inside Claude's preview, where it points to the hosted versions. On your own computer or host they are ignored.
- **Storage:** the loading screen uses `sessionStorage` to remember it has already played. If storage is unavailable, the page still works.
- **Browser support:** current versions of Chrome, Edge, Firefox and Safari.

## 🌙 The end
 
All stories, characters and pictures are original, written and illustrated with [Claude](https://www.anthropic.com/claude) by Anthropic.
 
Close the book when you are sleepy. Open it again when you are not.
