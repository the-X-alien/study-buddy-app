# Study Buddy - Deployment Guide

## Quickstart Deploy to Vercel (Recommended)

The easiest way to deploy Study Buddy:

```bash
# 1. Fork this repository
# 2. Clone your fork
git clone https://github.com/YOUR_USERNAME/study-buddy-app.git
cd study-buddy-app

# 3. Install Vercel CLI
npm i -g vercel

# 4. Deploy
vercel
```

Follow the prompts and Vercel will automatically:
- Build your app
- Deploy to a live URL
- Provide a production domain

## Deploy with GitHub Pages

1. Build the app: `npm run build`
2. Push to GitHub
3. Enable GitHub Pages in repository settings
4. Select `main` branch as source

## Using index.html Directly

The `index.html` file is a complete, self-contained React application that works without any build process:

1. Download `index.html`
2. Open in any web browser
3. Or upload to any web host (GitHub Pages, Netlify, Firebase Hosting, etc.)

## Environment Variables

For production with backend services:

```env
VITE_SUPABASE_URL=your_supabase_url
VITE_SUPABASE_ANON_KEY=your_supabase_key
VITE_OPENAI_API_KEY=your_openai_key  # Optional
```

## Production Checklist

- [ ] All features tested locally
- [ ] Environment variables configured
- [ ] API keys secured (never commit to git)
- [ ] Responsive design tested on mobile
- [ ] Performance optimized
- [ ] Analytics configured
- [ ] Custom domain set up (optional)

## Free Hosting Options

1. **Vercel** - Optimized for React, 1000 free deployments/month
2. **Netlify** - 100 GB bandwidth/month free
3. **GitHub Pages** - Free, built into GitHub
4. **Firebase Hosting** - 1 GB free storage
5. **Heroku** - Free tier available

## Troubleshooting

**Build fails?**
- Check Node.js version: `node --version` (should be 16+)
- Clear cache: `npm cache clean --force`
- Reinstall: `rm -rf node_modules && npm install`

**App not loading?**
- Check browser console for errors
- Verify all API endpoints are accessible
- Check CORS settings if using external API

## Support

Need help? Open an issue on GitHub or check the README for more information.
