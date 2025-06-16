# Deployment Guide

This guide covers different deployment options for the Civic Budget Allocation Platform.

## Option 1: GitHub Pages (Frontend Only)

**Note**: GitHub Pages only supports static sites, so the backend functionality will be limited. This option is best for demonstrations.

### Setup Steps:
1. Push your code to a GitHub repository
2. Go to repository Settings → Pages
3. Select "GitHub Actions" as the source
4. The included workflow will automatically deploy on push to main branch

### Limitations:
- No backend API functionality
- Uses in-memory data only (resets on page reload)
- Suitable for UI demonstrations

## Option 2: Vercel (Recommended for Full-Stack)

Vercel supports both frontend and serverless backend functions.

### Setup Steps:
1. Connect your GitHub repository to Vercel
2. Configure build settings:
   - **Build Command**: `npm run build`
   - **Output Directory**: `dist`
   - **Install Command**: `npm install`

### Environment Variables:
No additional environment variables needed for basic setup.

## Option 3: Railway

Railway provides full hosting for Node.js applications.

### Setup Steps:
1. Connect your GitHub repository to Railway
2. Railway will auto-detect the Node.js project
3. Set the start command: `npm run dev`
4. Deploy automatically on git push

## Option 4: Render

Render offers both static site and web service hosting.

### For Web Service (Full-Stack):
1. Connect GitHub repository
2. Select "Web Service"
3. Configure:
   - **Build Command**: `npm install && npm run build`
   - **Start Command**: `npm run dev`

## Option 5: Local Development

### Prerequisites:
- Node.js 18 or higher
- npm or yarn

### Commands:
```bash
# Install dependencies
npm install

# Start development server
npm run dev

# Build for production
npm run build

# Preview production build
npm run preview
```

## Environment Configuration

The application uses in-memory storage by default. For production use, consider:

1. **Database Integration**: Replace MemStorage with a proper database
2. **Session Management**: Implement proper user sessions
3. **Security**: Add authentication and authorization
4. **Monitoring**: Add logging and error tracking

## Port Configuration

- Development: `http://localhost:5000`
- The server automatically binds to `0.0.0.0` for deployment compatibility

## Troubleshooting

### Common Issues:

1. **Build Errors**: Ensure all dependencies are installed with `npm install`
2. **Port Issues**: The app uses port 5000 by default, configurable via environment
3. **API Errors**: Check that both frontend and backend are running in development

### Performance Tips:

1. Enable gzip compression for production
2. Use a CDN for static assets
3. Implement proper caching strategies
4. Monitor memory usage with the in-memory storage

## Security Considerations

For production deployment:
- Implement proper authentication
- Add rate limiting
- Use HTTPS
- Validate all user inputs
- Implement proper error handling