# RentMeet - Apartment Meeting Scheduler

A modern web application for scheduling apartment viewings and meetings between prospective tenants and landlords/agents. Built with React, Express.js, and TypeScript, featuring cross-timezone coordination and social media sharing.

## Features

- **Cross-Timezone Scheduling**: Schedule meetings across different time zones with automatic conversion
- **Multiple Meeting Types**: Support for in-person visits, virtual tours, and phone consultations
- **Social Media Sharing**: Easy sharing of property listings on Facebook, Twitter, and Instagram
- **Calendar Integration**: Interactive calendar with meeting management
- **Mobile Responsive**: Full mobile support with dedicated navigation
- **Real-time Updates**: Live meeting status updates and notifications

## Tech Stack

### Frontend
- **React 18** with TypeScript
- **Wouter** for client-side routing
- **Radix UI + shadcn/ui** for accessible components
- **Tailwind CSS** for styling
- **TanStack Query** for server state management
- **React Hook Form + Zod** for form validation

### Backend
- **Node.js + Express** with TypeScript
- **Drizzle ORM** for database operations
- **PostgreSQL** for production (in-memory storage for development)
- **Zod** for API validation

## Getting Started

### Prerequisites
- Node.js 20 or higher
- npm or yarn

### Installation

1. Clone the repository:
```bash
git clone https://github.com/yourusername/rentmeet.git
cd rentmeet
```

2. Install dependencies:
```bash
npm install
```

3. Start the development server:
```bash
npm run dev
```

The application will be available at `http://localhost:5000`

## Available Scripts

- `npm run dev` - Start development server with hot reload
- `npm run build` - Build for production
- `npm run start` - Start production server
- `npm run db:push` - Deploy database schema

## Project Structure

```
├── client/                 # Frontend React application
│   ├── src/
│   │   ├── components/     # Reusable UI components
│   │   ├── pages/          # Page components
│   │   ├── lib/            # Utilities and configuration
│   │   └── hooks/          # Custom React hooks
├── server/                 # Backend Express application
│   ├── index.ts           # Server entry point
│   ├── routes.ts          # API routes
│   └── storage.ts         # Data storage layer
├── shared/                 # Shared types and schemas
│   └── schema.ts          # Database schema and types
└── components.json        # shadcn/ui configuration
```

## Database Schema

### Properties
- `id` - Unique identifier
- `address` - Property address
- `description` - Property description
- `rent` - Monthly rent amount
- `location` - Area/district
- `imageUrl` - Property image URL

### Meetings
- `id` - Unique identifier
- `propertyId` - Reference to property
- `title` - Meeting title
- `type` - Meeting type (in-person, virtual, phone)
- `date` - Meeting date and time
- `attendees` - Array of attendee emails
- `timezone` - Meeting timezone
- `status` - Meeting status (pending, confirmed, cancelled)

## Features in Detail

### Meeting Scheduling
- Multi-step form with property selection
- Date and time picker with timezone awareness
- Attendee management with email validation
- Meeting type selection (in-person, virtual, phone)

### Social Sharing
- Direct sharing to Facebook, Twitter, and Instagram
- Copy-to-clipboard functionality
- Custom share URLs for each property

### Calendar Integration
- Mini calendar with meeting indicators
- Upcoming meetings sidebar
- Meeting status tracking

## Environment Variables

For production deployment, set the following environment variables:

```env
DATABASE_URL=your_postgresql_connection_string
NODE_ENV=production
```

## Deployment

The application is optimized for deployment on platforms like Replit, Vercel, or Heroku. The build process creates:

- `dist/public/` - Frontend static files
- `dist/index.js` - Backend server bundle

## Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)  
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Support

If you encounter any issues or have questions, please [open an issue](https://github.com/yourusername/rentmeet/issues) on GitHub.