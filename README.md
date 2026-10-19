# 🍲 Hungr!Deals

A responsive food and recipe finder. Search any dish, browse meals by category, and open a full recipe with step-by-step instructions and a YouTube video. Built with **vanilla JavaScript**, **Bootstrap 5** and [TheMealDB](https://www.themealdb.com/api.php) API. No frameworks, no build step.

🔗 **Live demo:** [rayhan-ui.github.io/hungry-deals](https://rayhan-ui.github.io/hungry-deals)

![Hungr!Deals screenshot](screenshots/home.png)

## ✨ Features

- 🔍 **Search by name**: type a dish (e.g. `pasta`, `chicken`) and press Enter or click Search
- 🗂️ **Browse by category**: all meal categories load on the home page; click one to see its meals
- 📖 **Recipe details**: full cooking instructions with a link to the YouTube tutorial
- ⚠️ **Friendly error handling**: separate messages for an empty search and for no matching meals
- 📱 **Fully responsive**: sticky navbar, adaptive card grid, and a two-column recipe layout on large screens
- 🎨 **Custom design** layered on top of Bootstrap (warm palette, serif headings, hover effects, smooth animations)

## 🛠️ Tech Stack

| Area | Tools |
|---|---|
| Markup | HTML5 |
| Styling | CSS3 (custom properties, Grid, `:has()`), Bootstrap 5.3 |
| Logic | JavaScript (ES6+): `fetch`, Promises, DOM manipulation |
| Data | [TheMealDB API](https://www.themealdb.com/api.php) (free, no API key needed) |
| Fonts | Fraunces and Figtree (Google Fonts) |

## 📂 Project Structure

```
hungry-deals/
├── index.html      # page structure
├── style.css       # custom styles on top of Bootstrap
├── script.js       # API calls and DOM rendering
└── README.md
```

## 🚀 Getting Started

No installation required.

```bash
# 1. Clone the repo
git clone https://github.com/rayhan-ui/hungry-deals.git

# 2. Go into the folder
cd hungry-deals

# 3. Open index.html in your browser
```

Or use the **Live Server** extension in VS Code for auto-reload while editing.

## 🔌 API Endpoints Used

| Purpose | Endpoint |
|---|---|
| Search meals by name | `search.php?s={name}` |
| List all categories | `categories.php` |
| Meals in a category | `filter.php?c={category}` |
| Full details of one meal | `lookup.php?i={id}` |

Base URL: `https://www.themealdb.com/api/json/v1/1/`

## 🧠 How It Works

1. On page load, the app fetches all categories and renders them as cards.
2. Searching calls `search.php`, and clicking a category calls `filter.php`. Both pass their result to the same `displayFood()` function, which renders meal cards.
3. If the API returns `null` (no match), an error message is shown instead.
4. Clicking a meal card calls `lookup.php` with its ID and shows the full recipe at the top of the page.

## 📚 What I Learned

- Fetching and handling data from a public REST API
- Rendering dynamic UI with template literals and `createElement`
- Handling `null` / empty API responses gracefully
- Controlling scroll behavior (`scrollTo`) around DOM updates
- Customizing Bootstrap with CSS variables instead of fighting its defaults
- Building responsive layouts with Grid and media queries

## 🔮 Future Improvements

- [ ] Favorites list saved in `localStorage`
- [ ] Loading spinner while data is fetching
- [ ] Ingredients list with measurements on the recipe page
- [ ] Filter by area/cuisine
- [ ] Dark mode toggle
- [ ] Refactor to `async/await` and split code into modules

## 🙏 Credits

- Recipe data and images: [TheMealDB](https://www.themealdb.com/)
- UI framework: [Bootstrap](https://getbootstrap.com/)
- Fonts: [Google Fonts](https://fonts.google.com/)

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

## 👤 Author

**Ray**
- GitHub: [@rayhan-ui](https://github.com/rayhan-ui)