# Maison Serein — design and presentation notes

A fictional restaurant website created as a single-page HTML and CSS course project. All restaurant details, dishes and prices are invented for this assignment.

## Files and opening the site

```text
restaurant/
├── index.html              Page content and structure
├── style.css               Colours, layout and responsive styles
├── images/                 Five local Pexels photographs
├── video/
│   └── cooking-plov.webm   Local cooking video
├── home-wireframe.svg      Clear desktop and mobile homepage wireframe
├── presentation-practice.md  Classroom presentation and live-edit practice
└── README.md               Design notes and media credits
```

Open `index.html` in a modern browser. Keep the entire folder together: the HTML uses relative paths to the CSS, photographs and video. The page, images, system fonts and video do not require an internet connection. The source and licence links in the video credit and this document do require internet access. The form is deliberately a demonstration: the button is disabled and no message is sent or saved.

## 1. Simple homepage wireframe

Open [home-wireframe.svg](home-wireframe.svg) for a clear desktop and mobile diagram. See [presentation-practice.md](presentation-practice.md) for a classroom walkthrough and live-edit practice.

Desktop first screen (on a phone the navigation wraps and the image moves below the text):

```text
┌──────────────────────────────────────────────────────────────┐
│ ✳ Maison Serein   Our story  The menu  Experience  Contact  │
├───────────────────────────────┬──────────────────────────────┤
│ A neighbourhood table         │                              │
│                               │  Candlelit restaurant       │
│ A little longer               │  photograph                  │
│ at the table.                 │                              │
│                               │                              │
│ Short introductory text       │                              │
│ [ Explore the menu ↗ ]        │                              │
│                               │                              │
│ — Made for unhurried evenings │  Image caption               │
└───────────────────────────────┴──────────────────────────────┘
       ↓ Story → Menu → Experience & video → Contact → Footer
```

## 2. Colour palette

| Role | Colour | Hex |
|---|---|---|
| Main background | Cream | `#F5F0E8` |
| Main text and button | Deep brown | `#302820` |
| Muted borders | Warm taupe | `#A79786` |
| Small accents | Terracotta | `#A75E45` |
| Menu background | Light beige | `#E5D8C7` |
| Contact background | Dark brown | `#392E28` |
| Light text | Soft white | `#FFFAF3` |

Additional muted browns are used for supporting text and fine rules. Main palette variables are at the top of `style.css`.

## 3. Typography

- **Headings and wordmark:** Georgia, with Times New Roman and a generic serif as fallbacks. The italic style adds a gentle, editorial quality.
- **Body and navigation:** Arial, with Helvetica and a generic sans-serif as fallbacks. These familiar system fonts keep the site readable without a font download.

The exact appearance may vary slightly between devices depending on installed fonts.

## 4. Audience and design concept

The site is aimed at young adults and couples who enjoy a peaceful setting, thoughtful food and an intimate evening. The original concept is an unhurried neighbourhood table: warm photography, candlelight, quiet typography, generous spacing and a menu that reads like a small editorial feature. The restrained graphic stars and thin rules give the brand a recognisable character without requiring a logo image.

The user-supplied Behance project was a mood reference for warmth and refinement. Its page returned an access restriction during research, so the design follows the written brief rather than reproducing its assets, wording or layout.

### Four design principles

- **Contrast:** dark brown type and buttons stand out against cream; the dark contact section marks a change in the page journey.
- **Repetition:** Georgia headings, fine rules, the star motif and warm colours recur across the page.
- **Alignment:** shared section widths and consistent text edges make the varied image and text layouts coherent.
- **Proximity:** each dish image, title, description and price stays together; contact labels sit next to their details and form fields.

## 5. How the code works

- `index.html` contains a header and navigation, then `main` with Home, About, Menu, Experience and Contact sections, followed by a footer. Each navigation `href` points to the matching section `id`.
- The three menu `article` elements group a photograph, dish title, description and price. The `alt` attributes describe the images.
- The native `<video controls>` element embeds the local WebM file. It has a poster, an accessible label, and a download fallback. The credit below it links to the original and its licence.
- Every form field has a matching `<label for="…">` and input `id`. The button is `type="button"` and disabled because there is no submission service.
- `style.css` starts with colour variables, then styles the header, hero, sections, form and footer. CSS Grid and Flexbox organise columns and alignment. The media queries at `800px` and `600px` adapt the layout to narrower screens. Images use `max-width: 100%` and `object-fit: cover` to fit their containers.
- Keyboard focus outlines and a skip link support navigation. Reduced-motion settings disable smooth scrolling.

## 6. Four live-edit examples

1. **Change a colour:** at the top of `style.css`, change `--cream:#f5f0e8;` to another hex value such as `--cream:#fff8ef;`. Save and refresh to see the main background change.
2. **Change a heading:** in `index.html`, find the `h1` containing `A little longer` and replace the text inside it. Keep the `<h1>`, `<br>` and `<i>` tags if you want to retain the same structure and styling.
3. **Change an image:** put a suitable new photo in `images/`, then replace `src="images/hero.jpg"` with its new path, for example `src="images/my-table.jpg"`. Update the `alt` description and add the new source and licence to the media list below. The `object-fit: cover` rule crops images to fit; check the result after replacement.
4. **Change a navigation link:** in the header, change `<a href="#menu">The menu</a>` to point to an existing section such as `<a href="#contact">Contact</a>`. The value after `#` must match an actual section `id`. To rename a section target instead, update its `id` and every link that points to it.

## 7. Media sources and licences

Five photographs were downloaded from Pexels and resized/compressed through Pexels image delivery. Pexels permits free use and modification under the [Pexels License](https://www.pexels.com/license/), subject to its restrictions; attribution is not required but is provided here. Photographs illustrate the fictional brand and do not depict the restaurant itself.

| Local file | Creator and source |
|---|---|
| `images/hero.jpg` | Alexandra Kollstrem, [The Interior of a Restaurant](https://www.pexels.com/photo/the-interior-of-a-restaurant-8856579/) |
| `images/about.jpg` | Daniil Kondrashin, [Cozy Restaurant Table with Candlelit Ambiance](https://www.pexels.com/photo/cozy-restaurant-table-with-candlelit-ambiance-30420679/) |
| `images/risotto.jpg` | Eva Bronzini, [Close-up of Dish in Plate on Table](https://www.pexels.com/photo/close-up-of-dish-in-plate-on-table-6216844/) |
| `images/fish.jpg` | Cristian Mihaila, [Fried Fish and Grilled Vegetables](https://www.pexels.com/photo/fried-fish-and-grilled-vegetables-11653557/) |
| `images/pear.jpg` | Sylwester Ficek, [Elegant Dessert: Poached Pear with Honey and Spices](https://www.pexels.com/photo/elegant-dessert-poached-pear-with-honey-and-spices-34535224/) |

**Video:** Lokk1y, [Cooking Plov](https://commons.wikimedia.org/wiki/File:Cooking_Plov.webm), [Creative Commons Attribution–ShareAlike 4.0 International](https://creativecommons.org/licenses/by-sa/4.0/). The original video file is included unchanged. It shows pilaf being cooked in Uzbekistan and is presented as a general cooking film, not footage of Maison Serein. If you adapt the video, follow the licence's attribution and share-alike conditions.

The stars, circles, lines and arrow marks are text/CSS graphics; no separate icon library is used.

