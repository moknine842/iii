# Secret Missions Multiplayer

## Overview

Secret Missions Multiplayer is a social party game built as a modern web application where players complete secret missions while trying to identify other players' missions. The game supports both local (shared device) and online multiplayer modes, designed for 4+ players per session. Players receive hidden objectives that must be completed discretely while simultaneously attempting to guess other participants' missions to eliminate them from the game.

## User Preferences

Preferred communication style: Simple, everyday language.

## System Architecture

### Frontend Architecture
- **Framework**: React 18 with TypeScript for type safety and modern development practices
- **Build System**: Vite for fast development and optimized production builds
- **UI Framework**: Shadcn/ui components built on Radix UI primitives for accessibility
- **Styling**: Tailwind CSS with custom gaming theme variables and dark/light mode support
- **State Management**: TanStack Query for server state management, React hooks for local state
- **Routing**: Wouter for lightweight client-side routing
- **Animations**: Framer Motion for smooth transitions and gaming feel

### Backend Architecture
- **Runtime**: Node.js with Express.js for RESTful API endpoints
- **Type Safety**: TypeScript throughout the entire stack with shared types
- **Build Process**: ESBuild for server bundling with external package handling
- **Development**: Hot module replacement and runtime error overlays for development efficiency

### Data Storage Solutions
- **Database**: PostgreSQL with Drizzle ORM for type-safe database operations
- **Connection**: Neon Database serverless PostgreSQL for cloud deployment
- **Session Storage**: Connect-pg-simple for PostgreSQL-backed session management
- **Schema**: Shared type definitions between client and server using Drizzle-Zod

### Design System
- **Component Library**: Custom components following gaming UI patterns inspired by Discord and Among Us
- **Color Palette**: Gaming-focused theme with vibrant purple accents, dark navy backgrounds, and status-specific colors
- **Typography**: Inter for readability with Orbitron accent font for gaming headers
- **Layout**: Card-based interfaces with consistent spacing using Tailwind utilities
- **Responsive**: Mobile-first design with adaptive layouts for various screen sizes

### Game Logic Architecture
- **Game States**: Centralized state management for game phases (mode selection, online flow selection, lobby creation/joining, gameplay, results)
- **Online Mode Flow**: Two-step process - first select create or join, then proceed to respective screens
- **Real-time Features**: Prepared for WebSocket integration for live multiplayer functionality
- **Mission System**: Modular mission assignment with difficulty levels and categories
- **Timer Management**: Configurable game timers with warning thresholds and visual feedback
- **Player Management**: Comprehensive player status tracking (active, eliminated, completed, host)
- **Avatar System**: Full avatar customization for online mode with 4 options (upload, camera, custom builder, initials), available before create/join and editable in lobby

## External Dependencies

### UI and Styling
- **@radix-ui/react-***: Comprehensive accessible component primitives for complex UI elements
- **tailwindcss**: Utility-first CSS framework with custom gaming theme configuration
- **class-variance-authority**: Type-safe variant API for component styling
- **framer-motion**: Animation library for smooth transitions and gaming effects

### Database and Backend
- **@neondatabase/serverless**: Serverless PostgreSQL driver optimized for edge deployments
- **drizzle-orm**: Type-safe ORM with PostgreSQL dialect support
- **drizzle-zod**: Schema validation bridge between Drizzle and Zod
- **connect-pg-simple**: PostgreSQL session store for Express sessions

### Development Tools
- **@tanstack/react-query**: Powerful data synchronization for server state management
- **@hookform/resolvers**: Form validation with React Hook Form integration
- **react-hook-form**: Performant forms with minimal re-renders
- **zod**: Runtime type validation for API endpoints and form schemas

### Game-Specific Libraries
- **date-fns**: Date manipulation for game timers and session management
- **lucide-react**: Consistent icon library for gaming UI elements
- **embla-carousel-react**: Touch-friendly carousels for game mode selection
- **cmdk**: Command palette component for quick actions

### Development Infrastructure
- **@replit/vite-plugin-***: Replit-specific development tools for error handling and debugging
- **tsx**: TypeScript execution for development server
- **nanoid**: Secure unique ID generation for game sessions and players