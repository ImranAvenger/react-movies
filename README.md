# 🎬 React Movies

A modern, responsive movie search application built with React, Vite, and TailwindCSS. Search through thousands of movies, view trending searches, and discover your next favorite film with data from The Movie Database (TMDB) API.

![React](https://img.shields.io/badge/React-19.2.0-blue)
![Vite](https://img.shields.io/badge/Vite-7.2.4-646CFF)
![TailwindCSS](https://img.shields.io/badge/TailwindCSS-4.1.18-38B2AC)
![Appwrite](https://img.shields.io/badge/Appwrite-22.0.0-F02E65)

## ✨ Features

- 🔍 **Real-time Search** - Search movies with debounced input for optimal performance
- 📊 **Trending Movies** - View the most searched movies tracked via Appwrite
- 🎯 **Movie Details** - Display ratings, release year, and language for each movie
- 📱 **Responsive Design** - Fully responsive UI built with TailwindCSS
- ⚡ **Fast Performance** - Powered by Vite for lightning-fast development and builds
- 🎨 **Modern UI** - Clean, gradient-based design with smooth animations

## 🛠️ Tech Stack

- **Frontend Framework**: React 19.2.0
- **Build Tool**: Vite 7.2.4
- **Styling**: TailwindCSS 4.1.18
- **Backend**: Appwrite (for trending movies tracking)
- **API**: The Movie Database (TMDB) API
- **Utilities**: react-use (for debounce hook)

## 📋 Prerequisites

Before you begin, ensure you have the following installed:
- Node.js (v16 or higher)
- npm or yarn package manager

You'll also need:
- A [TMDB API key](https://www.themoviedb.org/settings/api)
- An [Appwrite](https://appwrite.io/) account and project setup

## 🚀 Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/ImranAvenger/react-movies.git
cd react-movies
```

### 2. Install dependencies

```bash
npm install
```

### 3. Environment Setup

Create a `.env` file in the root directory with the following variables:

```env
# TMDB API Configuration
VITE_TMDB_API_KEY=your_tmdb_api_bearer_token_here

# Appwrite Configuration
VITE_APPWRITE_PROJECT_ID=your_appwrite_project_id
VITE_APPWRITE_DATABASE_ID=your_appwrite_database_id
VITE_APPWRITE_TABLE_ID=your_appwrite_table_id
```

#### Getting TMDB API Key:
1. Sign up at [TMDB](https://www.themoviedb.org/signup)
2. Go to Settings → API → Request an API Key
3. Copy your **API Read Access Token** (Bearer Token)

#### Setting up Appwrite:
1. Create an account at [Appwrite](https://cloud.appwrite.io/)
2. Create a new project and copy the Project ID
3. Create a database and collection with the following attributes:
   - `searchTerm` (String, required)
   - `count` (Integer, required)
   - `movie_id` (Integer, required)
   - `poster_url` (String, required)
   - `title` (String, optional)
4. Copy the Database ID and Collection ID

### 4. Run the development server

```bash
npm run dev
```

The application will be available at `http://localhost:5173`

## 📜 Available Scripts

- `npm run dev` - Start development server
- `npm run build` - Build for production
- `npm run preview` - Preview production build locally
- `npm run lint` - Run ESLint to check code quality

## 📁 Project Structure

```
react-movies/
├── public/              # Static assets
├── src/
│   ├── assets/          # Images and icons
│   ├── components/      # React components
│   │   ├── MovieCard.jsx    # Movie card component
│   │   ├── Search.jsx       # Search input component
│   │   └── Spinner.jsx      # Loading spinner
│   ├── App.jsx          # Main application component
│   ├── appwrite.js      # Appwrite configuration and functions
│   ├── index.css        # Global styles
│   └── main.jsx         # Application entry point
├── .env                 # Environment variables (create this)
├── eslint.config.js     # ESLint configuration
├── index.html           # HTML template
├── package.json         # Project dependencies
├── vite.config.js       # Vite configuration
└── README.md           # Project documentation
```

## 🎯 How It Works

1. **Search Functionality**: Users can search for movies using the search bar. The search is debounced to prevent excessive API calls.

2. **Movie Display**: Movies are fetched from TMDB API and displayed in a responsive grid layout with details like title, rating, release year, and language.

3. **Trending Tracking**: Each search query is tracked in Appwrite. The most searched movies are displayed in the trending section.

4. **Default View**: When no search term is entered, popular movies are displayed by default.

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the project
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📝 License

This project is open source and available under the [MIT License](LICENSE).

## 🙏 Acknowledgments

- [The Movie Database (TMDB)](https://www.themoviedb.org/) for providing the movie data API
- [Appwrite](https://appwrite.io/) for backend services
- [Vite](https://vitejs.dev/) for the blazing fast build tool
- [TailwindCSS](https://tailwindcss.com/) for the utility-first CSS framework

## 📧 Contact

For questions or suggestions, please open an issue in the repository.

---

Made with ❤️ using React and Vite
