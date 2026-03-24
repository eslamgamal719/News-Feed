# 📰 NewsFeed App

A modern news aggregator built with **React 19** and **Vite 8** that fetches real-time top headlines from [NewsAPI](https://newsapi.org/). Browse, search, and filter news articles by category — all in a clean, responsive Material UI interface.

---

## ✨ Features

- **Live Headlines** — Fetches top US headlines in real time from NewsAPI.
- **Category Filtering** — Filter articles by *General, Business, Entertainment, Health, Science, Sports,* or *Technology*.
- **Debounced Search** — Search articles by keyword with a 500 ms debounce to reduce unnecessary API calls.
- **Pagination** — Navigate through pages of results with Previous / Next controls.
- **Skeleton Loading** — Smooth loading placeholders while articles are being fetched.
- **Error Handling** — Graceful error messages displayed when the API request fails.
- **Responsive Layout** — Constrained to a max width of 768 px for comfortable reading on any device.

---

## 🛠️ Tech Stack

| Layer        | Technology                                         |
| ------------ | -------------------------------------------------- |
| Framework    | [React 19](https://react.dev/)                     |
| Build Tool   | [Vite 8](https://vite.dev/)                        |
| UI Library   | [MUI (Material UI) v7](https://mui.com/)           |
| Styling      | MUI `styled()` API + Emotion                       |
| Typography   | [Roboto](https://fonts.google.com/specimen/Roboto) via `@fontsource/roboto` |
| Utilities    | [Lodash](https://lodash.com/) (`debounce`)         |
| API          | [NewsAPI](https://newsapi.org/)                     |

---

## 📁 Project Structure

```
newsfeed_app/
├── index.html
├── .env                        # API keys (not committed)
├── package.json
├── vite.config.js
└── src/
    ├── main.jsx                # App entry point & font imports
    ├── App.jsx                 # Root component — data fetching, search, pagination
    ├── index.css               # Global styles
    └── components/
        ├── NewsHeader.jsx      # AppBar with title, category select & search input
        ├── NewsFeed.jsx        # Renders article list or loading skeletons
        ├── NewsArticle.jsx     # Individual article card with image, title & metadata
        ├── LoadingArticle.jsx  # Skeleton placeholder card
        └── StyledCard.jsx      # Reusable styled MUI Card
```

---

## 🚀 Getting Started

### Prerequisites

- **Node.js** ≥ 18
- A free API key from [NewsAPI](https://newsapi.org/register)

### Installation

```bash
# Clone the repository
git clone https://github.com/eslamgamal719/News-Feed.git
cd News-Feed

# Install dependencies
npm install
```

### Environment Variables

Create a `.env` file in the project root:

```env
VITE_NEWS_API_KEY2=your_newsapi_key_here
```

> **Note:** The app reads the key from `VITE_NEWS_API_KEY2`. You can obtain a free key at [newsapi.org](https://newsapi.org/register).

### Run the Dev Server

```bash
npm run dev
```

The app will be available at **http://localhost:5173** (default Vite port).

### Build for Production

```bash
npm run build
npm run preview   # preview the production build locally
```

---

## 📜 Available Scripts

| Command             | Description                        |
| ------------------- | ---------------------------------- |
| `npm run dev`       | Start the Vite development server  |
| `npm run build`     | Create an optimized production build |
| `npm run preview`   | Preview the production build locally |
| `npm run lint`      | Run ESLint across the project      |

---

## 📄 License

This project is open-source and available for personal and educational use.
