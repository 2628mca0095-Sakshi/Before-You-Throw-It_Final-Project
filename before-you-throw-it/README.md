# Before You Throw It

Frontend demonstration of a waste-reduction product: identify an everyday item, understand its condition, then choose reuse, repair, donation, resale, upcycling, or recycling before disposal.

Built with HTML5, CSS3, vanilla JavaScript (ES6+), Bootstrap 5, Bootstrap Icons, and Chart.js. No backend is required.

## Run locally

1. Open the `before-you-throw-it` folder in VS Code.
2. Start Live Server (or any static server) with `index.html` as the root.
3. Browse from the home page. Relative paths work from `index.html` and from files in `pages/`.

Do not open nested pages as `file://` without a server if the browser blocks module-like behaviour; a local server is the intended workflow.

## Main flow

1. Home explains the idea.
2. **Check an Item** searches the demo catalogue (20+ items), sets condition and preference.
3. **Recommendations** ranks next steps and can save an idea or log an action.
4. **DIY** filters upcycling projects.
5. **Sorting Guide** answers “where does this go?”
6. **Find a Place** shows demo drop-off points (no live maps API).
7. **My Impact** charts localStorage actions, estimates, and badges.
8. **Saved** and **Learn** keep lists and short articles.

## Data and future backend

Demo catalogues live in `js/items.js`. Persistence lives in `js/storage.js` (`localStorage` only).

Comments in the JavaScript mark where a later **Java Spring Boot + REST + MySQL** layer can replace demo data, for example:

- `GET /api/items`
- `POST /api/recommendations` (including a future AI model)
- `GET /api/places?city=`
- `GET/POST /api/actions`

Keep the current object shapes (`id`, `name`, `category`, `material`, `impactGrams`, and so on) so the UI does not need a redesign.

Impact numbers are **demo estimates**, not scientific measurements.

## Theme

Light/dark mode is stored as `byti_theme`. Colours are CSS variables in `css/style.css` and `css/dark-mode.css`.

## Project structure

See the folders `pages/`, `css/`, `js/`, and `images/` next to this file.
