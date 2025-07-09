# Moodify - Music Streaming Application

A full-stack music streaming application built with the MERN stack (MongoDB, Express, React, Node.js).

## Project Structure

This project is organized as a monorepo with separate frontend and backend directories:

- `/frontend` - React application built with Vite, TypeScript, and Tailwind CSS
- `/backend` - Express.js API server

## Deployment Instructions for Render

### Prerequisites

1. A [Render](https://render.com/) account
2. A MongoDB database (e.g., MongoDB Atlas)
3. A [Clerk](https://clerk.dev/) account for authentication
4. A [Cloudinary](https://cloudinary.com/) account for file storage

### Environment Variables

Before deploying, you need to set up the following environment variables in your Render dashboard:

- `PORT` - Port for the server (default: 5000)
- `NODE_ENV` - Set to "production"
- `MONGODB_URI` - Your MongoDB connection string
- `CLERK_SECRET_KEY` - Your Clerk secret key
- `ADMIN_EMAIL` - Email address for admin access
- `CLOUDINARY_CLOUD_NAME` - Your Cloudinary cloud name
- `CLOUDINARY_API_KEY` - Your Cloudinary API key
- `CLOUDINARY_API_SECRET` - Your Cloudinary API secret

Refer to the `.env.example` file for all required environment variables.

### Deployment Steps

1. **Connect your GitHub repository to Render**
   - Sign in to your Render account
   - Click "New" and select "Web Service"
   - Connect your GitHub repository

2. **Configure your Web Service**
   - Name: `moodify` (or your preferred name)
   - Environment: `Node`
   - Build Command: `npm run build`
   - Start Command: `npm start`
   - Set the environment variables listed above

3. **Deploy**
   - Click "Create Web Service"
   - Render will automatically build and deploy your application

## Local Development

### Installation

```bash
# Install dependencies for both frontend and backend
npm run build

# Start the development server
npm run dev
```

### Available Scripts

- `npm run build` - Install dependencies and build the frontend
- `npm start` - Start the production server
- `npm run dev` - Start the development server with hot reloading

## Features

- User authentication with Clerk
- Music streaming
- Album browsing
- Admin dashboard for managing songs and albums
- Real-time user activity tracking with Socket.io

## Technologies Used

### Frontend
- React 19
- TypeScript
- Vite
- Tailwind CSS
- Zustand for state management
- Socket.io client for real-time features

### Backend
- Express.js
- MongoDB with Mongoose
- Socket.io for real-time communication
- Clerk for authentication
- Cloudinary for file storage