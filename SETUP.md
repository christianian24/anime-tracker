# Setup Guide

## Environment Variables

To run this application, you need to create a `.env` file in the root directory with your Supabase credentials.

### 1. Create `.env` file

Create a file named `.env` in the root directory and add the following:

```env
REACT_APP_SUPABASE_URL=your_supabase_url_here
REACT_APP_SUPABASE_ANON_KEY=your_supabase_anon_key_here
```

### 2. Install Dependencies

```bash
npm install
# or
yarn install
```

### 3. Start Development Server

```bash
npm start
# or
yarn start
```

## Security Improvements Made

1. **API Keys**: Moved from hardcoded values to environment variables
2. **Error Handling**: Replaced `alert()` calls with proper toast notifications
3. **Code Duplication**: Created shared utilities for common operations
4. **Error Boundaries**: Added React error boundaries for better error handling
5. **User Feedback**: Improved user experience with toast notifications

## Database Schema

Make sure your Supabase database has the following tables:

### `profiles` table
```sql
CREATE TABLE profiles (
  id UUID REFERENCES auth.users(id) PRIMARY KEY,
  username TEXT,
  bio TEXT,
  avatar_url TEXT,
  banner_url TEXT,
  profile_color TEXT DEFAULT 'bg-blue-500',
  updated_at TIMESTAMP WITH TIME ZONE
);
```

### `anime_list` table
```sql
CREATE TABLE anime_list (
  id SERIAL PRIMARY KEY,
  user_id UUID REFERENCES auth.users(id),
  anilist_id INTEGER NOT NULL,
  status TEXT DEFAULT 'Plan to Watch',
  episodes_watched INTEGER DEFAULT 0,
  rating INTEGER,
  anime_data JSONB,
  updated_at TIMESTAMP WITH TIME ZONE DEFAULT NOW(),
  UNIQUE(user_id, anilist_id)
);
```

## Storage Buckets

Create the following storage buckets in Supabase:
- `avatars` - for user profile pictures
- `banners` - for user banner images

## Features

- ✅ User authentication with Supabase
- ✅ Anime search and discovery
- ✅ Personal anime list management
- ✅ Profile customization
- ✅ Image upload and cropping
- ✅ Responsive design
- ✅ Toast notifications
- ✅ Error boundaries
- ✅ Secure API key management 