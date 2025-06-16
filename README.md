# Civic Budget Allocation Platform

An interactive civic budget allocation platform designed to democratize local decision-making through technology. The platform enables community members to collaboratively prioritize and fund local proposals with intuitive, engaging interfaces.

## Features

- **Interactive Budget Allocation**: Users can allocate a $16,000 budget across community proposals
- **Real-time Progress Tracking**: Visual progress bars and budget tracking
- **Admin Dashboard**: Comprehensive reporting and analytics interface
- **Responsive Design**: Works seamlessly on desktop and mobile devices
- **Data Visualization**: Charts showing proposal popularity and funding distribution

## Technical Stack

- **Frontend**: React 18 with Vite
- **Backend**: Express.js
- **Language**: TypeScript
- **UI Components**: Shadcn/UI with Tailwind CSS
- **Charts**: Recharts
- **Routing**: Wouter
- **State Management**: TanStack Query (React Query)

## Quick Start

1. **Clone the repository**
   ```bash
   git clone <your-repo-url>
   cd civic-budget-platform
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Start the development server**
   ```bash
   npm run dev
   ```

4. **Open your browser**
   Navigate to `http://localhost:5000`

## Project Structure

```
├── client/                 # Frontend React application
│   ├── src/
│   │   ├── components/     # Reusable UI components
│   │   ├── pages/          # Page components
│   │   ├── lib/            # Utility functions
│   │   └── hooks/          # Custom React hooks
├── server/                 # Backend Express application
│   ├── index.ts           # Server entry point
│   ├── routes.ts          # API routes
│   └── storage.ts         # In-memory data storage
├── shared/                # Shared types and schemas
│   └── schema.ts          # Database schemas and types
└── package.json           # Dependencies and scripts
```

## Available Scripts

- `npm run dev` - Start development server (frontend + backend)
- `npm run build` - Build for production
- `npm run preview` - Preview production build

## API Endpoints

### Proposals
- `GET /api/proposals` - Get all proposals
- `POST /api/proposals` - Create new proposal

### Budget Allocations
- `GET /api/budget-allocations` - Get current user's allocations
- `POST /api/budget-allocations` - Create/update allocation
- `DELETE /api/budget-allocations/:id` - Delete allocation
- `GET /api/all-allocations` - Get all allocations (admin)

## Data Model

The application uses three main data entities:

- **Users**: Basic user information
- **Proposals**: Community proposals with funding requirements
- **Budget Allocations**: User budget allocations per proposal

## Configuration

The application uses in-memory storage by default with sample data. For production deployment, you may want to integrate with a proper database.

## Sample Data

The application comes pre-loaded with sample proposals including:
- Community garden improvements
- Public park renovations
- Local business support programs
- Transportation improvements
- Community center upgrades

## Deployment

### GitHub Pages (Static Deployment)
1. Build the project: `npm run build`
2. Deploy the `dist` folder to GitHub Pages

### Vercel/Netlify
1. Connect your GitHub repository
2. Set build command: `npm run build`
3. Set output directory: `dist`

### Railway/Render (Full-stack)
1. Connect your GitHub repository
2. Set start command: `npm run dev`
3. Ensure port configuration matches your hosting platform

## Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Test thoroughly
5. Submit a pull request

## License

MIT License - feel free to use this code for your civic engagement projects.

## Support

For questions or issues, please open a GitHub issue or contact the development team.