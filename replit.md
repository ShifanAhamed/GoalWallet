# Overview

GoalWallet is a full-stack web application that combines a savings wallet system with goal-oriented financial planning. Users can create accounts, manage a digital wallet, set financial goals, and track their progress toward achieving those goals. The application features secure authentication, payment processing through Razorpay, and a comprehensive savings management system.

# User Preferences

Preferred communication style: Simple, everyday language.

# System Architecture

## Frontend Architecture
The client-side is built with React 18 using TypeScript and Vite as the build tool. It follows a component-based architecture with:
- **UI Framework**: shadcn/ui components built on Radix UI primitives for consistent, accessible design
- **Styling**: Tailwind CSS with a custom design system using CSS custom properties for theming
- **State Management**: Zustand for authentication state with persistence
- **Data Fetching**: TanStack Query (React Query) for server state management and caching
- **Routing**: Wouter for lightweight client-side routing
- **Forms**: React Hook Form with Zod validation for type-safe form handling

## Backend Architecture
The server is built with Express.js following a RESTful API pattern:
- **Framework**: Express.js with TypeScript support
- **Authentication**: JWT-based authentication with bcrypt password hashing
- **Database Layer**: Drizzle ORM with type-safe database operations
- **API Structure**: Organized route handlers with middleware for authentication
- **Error Handling**: Centralized error handling middleware

## Data Storage Solutions
- **Database**: PostgreSQL with Neon serverless hosting
- **ORM**: Drizzle ORM for type-safe database queries and migrations
- **Schema Design**: Relational design with users, wallets, goals, and transactions tables
- **Connection Management**: Connection pooling through Neon's serverless driver

## Authentication and Authorization
- **JWT Tokens**: Stateless authentication with JWT tokens
- **Password Security**: bcrypt hashing with salt rounds for password storage
- **Session Management**: Client-side token storage with automatic expiration handling
- **Protected Routes**: Middleware-based route protection on both client and server

## External Dependencies

### Payment Processing
- **Razorpay**: Payment gateway integration for wallet deposits and transactions
- **Payment Methods**: Support for UPI, cards, and net banking
- **Order Management**: Razorpay order creation and payment verification

### Database Services
- **Neon Database**: Serverless PostgreSQL hosting with connection pooling
- **Database URL**: Environment-based connection string configuration

### Development Tools
- **Vite**: Fast development server with HMR and optimized builds
- **TypeScript**: Full-stack type safety with shared types
- **Replit Integration**: Development environment integration with runtime error overlay

### UI and Styling
- **Radix UI**: Headless UI primitives for accessibility and keyboard navigation
- **Tailwind CSS**: Utility-first CSS framework with custom design tokens
- **Lucide Icons**: Consistent icon library throughout the application
- **Google Fonts**: Inter font family for typography