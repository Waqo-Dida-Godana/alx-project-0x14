# CineSeek - Movie Discovery Application

A modern movie discovery application built with Next.js, TypeScript, and Tailwind CSS that integrates with the MoviesDatabase API.

## Features

- 🎬 Browse and discover movies
- 🔍 Filter by year and genre
- 📱 Fully responsive design
- ⚡ Fast and optimized with Next.js
- 🎨 Beautiful UI with Tailwind CSS
- 🔗 Integration with MoviesDatabase API

## Tech Stack

- **Framework**: Next.js 16 (Pages Router)
- **Language**: TypeScript
- **Styling**: Tailwind CSS v3
- **Icons**: Font Awesome
- **Package Manager**: npm

## Getting Started

### Prerequisites

- Node.js (v18 or higher)
- npm
- MoviesDatabase API key from [RapidAPI](https://rapidapi.com)

### Installation

1. Clone the repository:
```bash
cd alx-movie-app
```

2. Install dependencies:
```bash
npm install
```

3. Set up environment variables:
   - Copy `.env.local` and add your API key:
   ```
   MOVIE_API_KEY=your_api_key_here
   ```

4. Run the development server:
```bash
npm run dev
```

5. Open [http://localhost:3000](http://localhost:3000) in your browser

## Project Structure

```
alx-movie-app/
├── components/
│   ├── commons/          # Reusable components
│   │   ├── Button.tsx
│   │   ├── Loading.tsx
│   │   └── MovieCard.tsx
│   └── layouts/          # Layout components
│       ├── Header.tsx
│       ├── Footer.tsx
│       └── Layout.tsx
├── interfaces/           # TypeScript interfaces
│   └── index.ts
├── pages/
│   ├── api/             # API routes
│   │   └── fetch-movies.ts
│   ├── movies/          # Movies page
│   │   └── index.tsx
│   ├── _app.tsx         # App wrapper
│   └── index.tsx        # Landing page
├── public/              # Static assets
├── styles/              # Global styles
│   └── globals.css
└── tailwind.config.js   # Tailwind configuration
```

## Available Scripts

- `npm run dev` - Start development server
- `npm run build` - Build for production
- `npm start` - Start production server
- `npm run lint` - Run ESLint

## API Integration

The app uses the MoviesDatabase API from RapidAPI. Make sure to:
1. Sign up at [RapidAPI](https://rapidapi.com)
2. Subscribe to the MoviesDatabase API
3. Add your API key to `.env.local`

## Features Overview

### Landing Page
- Hero section with call-to-action
- Sign-up section
- Responsive navigation

### Movies Page
- Grid layout of movie cards
- Filter by year (2019-2024)
- Filter by genre (All, Animation, Comedy, Fantasy)
- Pagination support
- Loading states

### Components
- **Header**: Navigation with logo and menu
- **Footer**: Links and social media icons
- **MovieCard**: Display movie poster, title, and year
- **Button**: Reusable button component
- **Loading**: Loading overlay with animation

## Environment Variables

Required environment variables in `.env.local`:

```
MOVIE_API_KEY=your_rapidapi_key_here
```

## License

This project is part of the ALX Software Engineering program.

## Acknowledgments

- MoviesDatabase API by RapidAPI
- Next.js team
- Tailwind CSS team
- Font Awesome