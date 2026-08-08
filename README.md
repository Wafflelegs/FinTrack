# FinTrack — Personal Expense Tracker

A responsive, premium-looking expense tracker dashboard built with **HTML5, CSS3, Vanilla JavaScript (ES6)** and **LocalStorage**. No backend, no build step required for the app itself.

## Features

- Dummy login screen with session persistence
- Dashboard with animated stat counters and spending insights
- Full transaction CRUD (add, edit, delete)
- Live search, category/type/date filters and sorting
- Chart.js visualisations: category pie, income vs expense doughnut, monthly bar, cashflow line
- Monthly budget module with progress bars and 80% / 100% warnings
- Reports with CSV and JSON export
- Profile page with avatar upload (stored as data URL)
- Light/dark theme, glassmorphism UI, Poppins + Font Awesome
- Keyboard shortcuts: `Ctrl+N` new transaction, `Ctrl+F` search, `Ctrl+D` theme

## Project structure

```
public/app/
├── index.html          # main dashboard shell
├── login.html          # login screen
├── css/
│   ├── style.css       # design system, layout, components
│   └── responsive.css  # mobile / tablet / desktop breakpoints
└── js/
    ├── utils.js        # helpers: formatting, toasts, counters, export
    ├── storage.js      # LocalStorage data layer
    ├── auth.js         # login / logout / theme
    ├── charts.js       # Chart.js rendering
    ├── budget.js       # budget calculations
    ├── dashboard.js    # stats and insights
    ├── settings.js     # preferences, categories, profile, reports
    └── script.js       # main controller: routing, CRUD, filters
```

## Running locally

The app is fully static. Either open `public/app/login.html` directly in a browser, or serve the folder:

```sh
npx serve public/app
```

Then visit the printed URL and sign in on the login screen.

## Data storage

All data (transactions, budget, profile, categories, preferences) lives in the browser's LocalStorage under namespaced keys. Imported backup files are validated and sanitised before being saved.

## Tech

HTML5 · CSS3 · JavaScript (ES6) · Chart.js · Font Awesome · Google Fonts (Poppins) · LocalStorage
