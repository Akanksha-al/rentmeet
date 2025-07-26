# RentMeet - Apartment Meeting Scheduler

## Overview

RentMeet is a full-stack web application for scheduling apartment viewings and meetings between prospective tenants and landlords/agents. The application facilitates cross-timezone meeting coordination with a modern, responsive interface built using React and Express.js.

## User Preferences

Preferred communication style: Simple, everyday language.

## System Architecture

### Frontend Architecture
- **Framework**: React 18 with TypeScript
- **Routing**: Wouter for client-side routing
- **UI Components**: Radix UI primitives with shadcn/ui component library
- **Styling**: Tailwind CSS with CSS custom properties for theming
- **State Management**: TanStack Query (React Query) for server state management
- **Form Handling**: React Hook Form with Zod validation
- **Build Tool**: Vite with custom configuration for development and production

### Backend Architecture
- **Runtime**: Node.js with Express.js framework
- **Language**: TypeScript with ES modules
- **API Design**: RESTful API endpoints following conventional patterns
- **Development**: Hot module replacement via Vite middleware integration

### Data Storage
- **Database**: PostgreSQL (configured via Drizzle ORM)
- **ORM**: Drizzle ORM with type-safe schema definitions
- **Development Storage**: In-memory storage implementation for development/testing
- **Migrations**: Drizzle Kit for database schema management

## Key Components

### Database Schema
- **Properties Table**: Stores rental property information (address, description, rent, location, images)
- **Meetings Table**: Stores meeting details with foreign key reference to properties
- **Schema Features**: UUID primary keys, JSON arrays for attendees, timezone support, timestamps

### API Endpoints
- **Properties**: CRUD operations for rental property management
- **Meetings**: Full meeting lifecycle management (create, read, update, delete)
- **Validation**: Zod schema validation for all API inputs

### Frontend Components
- **Calendar Integration**: Custom calendar sidebar with meeting display
- **Meeting Form**: Multi-step form with timezone selection and attendee management
- **Property Display**: Cards and detailed views for rental properties
- **Social Sharing**: Integration for sharing property listings
- **Mobile Navigation**: Responsive bottom navigation for mobile devices

### Authentication & Authorization
- **Current State**: No authentication implemented (development phase)
- **Session Management**: Express session configuration present but not utilized

## Data Flow

1. **Client Requests**: React components use TanStack Query to fetch data from API endpoints
2. **API Processing**: Express routes handle requests, validate input with Zod schemas
3. **Data Storage**: Currently uses in-memory storage, designed for PostgreSQL integration
4. **Response**: JSON responses sent back to client with error handling
5. **State Updates**: TanStack Query manages cache invalidation and UI updates

## External Dependencies

### Core Framework Dependencies
- **@neondatabase/serverless**: Serverless PostgreSQL driver for Neon
- **drizzle-orm**: Type-safe database ORM
- **@tanstack/react-query**: Server state management
- **react-hook-form**: Form state management
- **zod**: Runtime type validation

### UI Dependencies
- **@radix-ui/***: Headless UI component primitives
- **tailwindcss**: Utility-first CSS framework
- **lucide-react**: Icon library
- **date-fns**: Date manipulation utilities

### Development Dependencies
- **vite**: Build tool and development server
- **tsx**: TypeScript execution for Node.js
- **esbuild**: JavaScript bundler for production builds

## Deployment Strategy

### Development Environment
- **Frontend**: Vite development server with HMR
- **Backend**: Node.js with tsx for TypeScript execution
- **Database**: In-memory storage for rapid development

### Production Build
- **Frontend**: Vite build output to `dist/public`
- **Backend**: esbuild compilation to `dist/index.js`
- **Database**: PostgreSQL via Neon serverless driver
- **Environment**: Requires `DATABASE_URL` environment variable

### Build Commands
- `npm run dev`: Development mode with hot reload
- `npm run build`: Production build for both frontend and backend
- `npm run start`: Production server execution
- `npm run db:push`: Database schema deployment

### Configuration Requirements
- Environment variables for database connection
- Proper setup of PostgreSQL database (Neon recommended)
- Static file serving configuration for production deployment