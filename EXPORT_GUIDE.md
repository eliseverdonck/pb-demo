# Export Guide - Download and Deploy to GitHub

## Quick Download Steps

1. **Download Project Files**
   - Download all files from this Replit project
   - Maintain the exact folder structure shown below

2. **Required Project Structure**
   ```
   civic-budget-platform/
   ├── client/
   │   └── src/
   │       ├── components/
   │       ├── pages/
   │       ├── lib/
   │       └── hooks/
   ├── server/
   ├── shared/
   ├── .github/workflows/
   ├── package.json
   ├── package-lock.json
   ├── vite.config.ts
   ├── tsconfig.json
   ├── tailwind.config.ts
   ├── postcss.config.js
   ├── README.md
   └── DEPLOYMENT.md
   ```

## GitHub Repository Setup

1. **Create New Repository**
   ```bash
   # On GitHub, create a new repository named "civic-budget-platform"
   # Clone it locally
   git clone https://github.com/YOUR_USERNAME/civic-budget-platform.git
   cd civic-budget-platform
   ```

2. **Add Project Files**
   - Copy all downloaded files into the cloned repository
   - Ensure file structure matches exactly

3. **Initial Commit**
   ```bash
   git add .
   git commit -m "Initial commit: Civic Budget Allocation Platform"
   git push origin main
   ```

## Local Development Setup

After downloading, run these commands:

```bash
# Install dependencies
npm install

# Start development server
npm run dev

# Open browser to http://localhost:5000
```

## Deployment Options

### Option A: GitHub Pages (Static Demo)
- Push to GitHub
- Enable Pages in repository settings
- Select "GitHub Actions" as source
- Automatic deployment on push to main

### Option B: Vercel (Full-Stack - Recommended)
- Connect GitHub repo to Vercel
- Automatic detection and deployment
- Full backend functionality preserved

### Option C: Railway
- Connect GitHub repo to Railway
- One-click deployment with full functionality

## Files to Download

**Essential Files:**
- All files in `client/` folder
- All files in `server/` folder  
- All files in `shared/` folder
- `package.json` and `package-lock.json`
- `vite.config.ts`
- `tsconfig.json`
- `tailwind.config.ts`
- `postcss.config.js`
- `components.json`
- `.github/workflows/deploy.yml`
- `README.md`
- `DEPLOYMENT.md`

**Optional:**
- `.gitignore`
- `.replit` (not needed for GitHub)

## Verification Steps

After setup, verify:
1. `npm install` runs without errors
2. `npm run dev` starts both frontend and backend
3. Navigate to proposals page works
4. Budget allocation functionality works
5. Dashboard displays charts and data
6. Navigation between pages works

## Support

If you encounter issues:
1. Check all files copied correctly
2. Verify Node.js version (18+ required)
3. Run `npm install` to ensure dependencies
4. Check console for specific error messages