# 🎌 AnimeTracker Pro

> A modern, full-stack anime tracking application built with React and Supabase, featuring real-time data synchronization, advanced filtering, and a beautiful responsive UI.

[![React](https://img.shields.io/badge/React-19.1.0-61DAFB?logo=react)](https://reactjs.org/)
[![Supabase](https://img.shields.io/badge/Supabase-2.50.5-3ECF8E?logo=supabase)](https://supabase.com/)
[![Tailwind CSS](https://img.shields.io/badge/Tailwind-3.4.17-38B2AC?logo=tailwind-css)](https://tailwindcss.com/)
[![TypeScript](https://img.shields.io/badge/TypeScript-5.0-3178C6?logo=typescript)](https://www.typescriptlang.org/)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

<div align="center">
  <img src="https://img.shields.io/badge/Status-Production%20Ready-brightgreen" alt="Production Ready" />
  <img src="https://img.shields.io/badge/Deployment-GitHub%20Pages-blue" alt="Deployed on GitHub Pages" />
  <img src="https://img.shields.io/badge/Testing-Jest%20%7C%20React%20Testing%20Library-orange" alt="Testing" />
</div>

## ✨ Features

### 🎯 Core Functionality
- **Real-time Anime Tracking** - Sync your watchlist across devices with Supabase
- **Advanced Search & Discovery** - Find anime with intelligent filtering and recommendations
- **Progress Management** - Track episodes watched, ratings, and watch status
- **User Profiles** - Customizable profiles with activity graphs and statistics

### 🎨 User Experience
- **Responsive Design** - Optimized for desktop, tablet, and mobile devices
- **Dark Theme** - Eye-friendly dark interface with customizable accent colors
- **Image Cropping** - Built-in avatar and banner image editor
- **Toast Notifications** - Real-time feedback for user actions
- **Skeleton Loading** - Smooth loading states for better perceived performance

### 🔧 Technical Excellence
- **Modern React Patterns** - Hooks, Context API, and functional components
- **State Management** - Optimistic UI updates with rollback on errors
- **Form Validation** - Comprehensive client-side validation
- **Error Boundaries** - Graceful error handling and recovery
- **Performance Optimized** - Code splitting, lazy loading, and memoization

## 🚀 Live Demo

**[View Live Application](https://christianian24.github.io/anime-tracker)**

## 🛠️ Tech Stack

### Frontend
- **React 19.1.0** - Latest React with concurrent features
- **React Router v6** - Client-side routing with nested routes
- **Tailwind CSS** - Utility-first CSS framework
- **Lucide React** - Beautiful, customizable icons
- **React Easy Crop** - Image cropping functionality

### Backend & Data
- **Supabase** - Backend-as-a-Service with PostgreSQL
- **GraphQL** - Efficient data fetching with GraphQL Request
- **Real-time Subscriptions** - Live data updates

### Development & Testing
- **Jest** - Unit and integration testing
- **React Testing Library** - Component testing best practices
- **ESLint** - Code quality and consistency
- **GitHub Pages** - Automated deployment

## 📦 Installation

### Prerequisites
- Node.js 18+ 
- npm or yarn
- Supabase account

### Setup

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/anime-tracker.git
   cd anime-tracker
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Environment Configuration**
   ```bash
   cp .env.example .env
   ```
   
   Fill in your Supabase credentials:
   ```env
   REACT_APP_SUPABASE_URL=your_supabase_url
   REACT_APP_SUPABASE_ANON_KEY=your_supabase_anon_key
   ```

4. **Start development server**
   ```bash
   npm start
   ```

5. **Open your browser**
   Navigate to [http://localhost:3000](http://localhost:3000)

## 🧪 Testing

```bash
# Run tests in watch mode
npm test

# Run tests with coverage
npm run test:coverage

# Run tests in CI mode
npm run test:ci
```

## 🏗️ Project Structure

```
src/
├── components/          # Reusable UI components
│   ├── ActivityGraph.js # User activity visualization
│   ├── AnimeCard.js     # Anime display component
│   ├── ImageCropper.js  # Image editing functionality
│   ├── Navbar.js        # Navigation component
│   └── Toast.js         # Notification system
├── context/             # React Context providers
│   └── AuthContext.js   # Authentication state management
├── pages/               # Route components
│   ├── DashboardPage.js # Main dashboard
│   ├── ProfilePage.js   # User profile management
│   ├── SearchPage.js    # Anime search interface
│   └── SettingsPage.js  # User settings
├── services/            # API and external services
│   ├── supabase.js      # Supabase client configuration
│   └── userService.js   # User-related API calls
└── utils/               # Utility functions
    ├── animeUtils.js    # Anime data processing
    └── imageUtils.js    # Image handling utilities
```

## 🔑 Key Features Deep Dive

### Real-time Data Synchronization
The app uses Supabase's real-time subscriptions to keep user data synchronized across sessions and devices. Changes to watchlists, ratings, and progress are immediately reflected in the UI.

### Optimistic UI Updates
Implemented optimistic updates for better user experience - UI changes are applied immediately while API calls happen in the background. Failed operations automatically rollback with user notification.

### Advanced Filtering System
Multi-criteria filtering including:
- Status-based filtering (Watching, Completed, On Hold, etc.)
- Title search with fuzzy matching
- Format filtering (TV, Movie, OVA, etc.)
- Rating-based sorting

### Image Management
Built-in image cropping and optimization:
- Avatar and banner image upload
- Aspect ratio enforcement
- Client-side image processing
- Automatic cache busting for updated images

## 🚀 Deployment

The application is automatically deployed to GitHub Pages on every push to the main branch.

```bash
# Build for production
npm run build

# Deploy to GitHub Pages
npm run deploy
```

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- [AniList API](https://anilist.gitbook.io/anilist-apiv2-docs/) for anime data
- [Supabase](https://supabase.com/) for backend services
- [Tailwind CSS](https://tailwindcss.com/) for styling
- [Lucide](https://lucide.dev/) for beautiful icons

## 📞 Contact

- **GitHub**: [@christianian24](https://github.com/christianian24)
- **Project Link**: [https://github.com/christianian24/anime-tracker](https://github.com/christianian24/anime-tracker)

---

<div align="center">
  <p>Made with ❤️ by <a href="https://github.com/christianian24">Christian Ian</a></p>
  <p>If you find this project helpful, please give it a ⭐️</p>
</div>

## Environment Variables

Copy `.env.example` to `.env` and fill in your Supabase credentials:

REACT_APP_SUPABASE_URL=...
REACT_APP_SUPABASE_ANON_KEY=...
