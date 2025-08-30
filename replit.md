# JT Enhancer

## Overview

JT Enhancer is a full-stack web application that allows users to upload photos and enhance them using AI-powered technology. The application provides a mobile-first user experience with image comparison features, real-time processing status, and integrated advertising through AdMob. Users can upload images via file selection or camera capture, process them through an AI enhancement pipeline, and download the improved results.

## User Preferences

Preferred communication style: Simple, everyday language.

## System Architecture

### Frontend Architecture
- **Framework**: React with TypeScript using Vite as the build tool
- **UI Library**: shadcn/ui components built on Radix UI primitives
- **Styling**: Tailwind CSS with CSS variables for theming
- **State Management**: TanStack Query for server state and React hooks for local state
- **Routing**: Wouter for lightweight client-side routing
- **Mobile-First Design**: Progressive Web App (PWA) capabilities with service worker

### Backend Architecture
- **Runtime**: Node.js with Express.js framework
- **Language**: TypeScript with ES modules
- **API Design**: RESTful endpoints for image upload, enhancement, and status polling
- **File Processing**: Multer for file uploads with Sharp for image optimization
- **Development Mode**: Vite integration for hot module replacement

### Data Storage Solutions
- **Database**: PostgreSQL with Drizzle ORM for type-safe database operations
- **Schema**: Users table for authentication and enhancements table for tracking image processing
- **File Storage**: Local filesystem with processed images served via Express static middleware
- **Session Management**: connect-pg-simple for PostgreSQL-based session storage

### Authentication and Authorization
- **Session-Based**: Traditional server-side sessions stored in PostgreSQL
- **User Management**: Username/password authentication with hashed passwords
- **Privacy Controls**: Public/private image settings for user content

### Image Processing Pipeline
- **Upload Processing**: Sharp library for image standardization (JPEG, quality optimization, size constraints)
- **AI Enhancement**: Placeholder infrastructure for AI model integration
- **Status Tracking**: Real-time polling system for processing status updates
- **File Management**: Organized upload directory structure with processed image variants

### Mobile and Progressive Web App Features
- **PWA Manifest**: Configurable app installation with custom icons and branding
- **Service Worker**: Offline caching strategy for core application assets
- **Camera Integration**: Native device camera access for photo capture
- **Touch-Optimized**: Mobile-first UI with gesture-friendly interactions

## External Dependencies

### Core Framework Dependencies
- **@neondatabase/serverless**: Neon PostgreSQL serverless driver for database connectivity
- **drizzle-orm**: Type-safe ORM with PostgreSQL dialect support
- **sharp**: High-performance image processing library for optimization and format conversion
- **multer**: Express middleware for handling multipart/form-data file uploads

### UI and Styling Dependencies
- **@radix-ui/***: Comprehensive set of unstyled, accessible UI primitives
- **tailwindcss**: Utility-first CSS framework with custom design system
- **class-variance-authority**: Type-safe variant API for component styling
- **lucide-react**: Modern icon library with consistent design language

### Development and Build Tools
- **vite**: Fast build tool with hot module replacement and modern ES features
- **tsx**: TypeScript execution engine for development server
- **esbuild**: Fast JavaScript bundler for production builds
- **@replit/vite-plugin-***: Replit-specific development enhancements

### Third-Party Integrations
- **AdMob**: Mobile advertising platform for banner and interstitial ads
- **TanStack Query**: Server state management with caching and synchronization
- **React Hook Form**: Form state management with validation support
- **date-fns**: Modern date utility library for time formatting

### Database and Session Management
- **connect-pg-simple**: PostgreSQL session store for Express sessions
- **drizzle-kit**: Database migration and schema management tools
- **zod**: Runtime type validation and schema definition