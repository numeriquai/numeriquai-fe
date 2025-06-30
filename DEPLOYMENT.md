# Deployment Guide

This guide provides instructions for deploying the Numeriquai website to various hosting platforms.

## Prerequisites

1. Build the project for production:
```bash
npm run build
```

This creates optimized files in the `dist/` directory.

## Deployment Options

### 1. Netlify (Recommended)

1. **Drag & Drop Method:**
   - Go to [netlify.com](https://netlify.com)
   - Drag the `dist/` folder to the deployment area
   - Your site will be live instantly

2. **Git Integration:**
   - Connect your GitHub repository
   - Set build command: `npm run build`
   - Set publish directory: `dist`
   - Deploy automatically on every push

### 2. Vercel

1. Install Vercel CLI:
```bash
npm i -g vercel
```

2. Deploy:
```bash
vercel
```

3. Follow the prompts and select the `dist` directory

### 3. GitHub Pages

1. Create a GitHub repository
2. Push your code
3. Go to Settings > Pages
4. Set source to "GitHub Actions"
5. Create `.github/workflows/deploy.yml`:

```yaml
name: Deploy to GitHub Pages

on:
  push:
    branches: [ main ]

jobs:
  build-and-deploy:
    runs-on: ubuntu-latest
    steps:
    - uses: actions/checkout@v2
    - uses: actions/setup-node@v2
      with:
        node-version: '16'
    - run: npm install
    - run: npm run build
    - uses: peaceiris/actions-gh-pages@v3
      with:
        github_token: ${{ secrets.GITHUB_TOKEN }}
        publish_dir: ./dist
```

### 4. AWS S3 + CloudFront

1. Create an S3 bucket
2. Enable static website hosting
3. Upload contents of `dist/` folder
4. Set bucket policy for public read access
5. (Optional) Set up CloudFront for CDN

### 5. Traditional Web Server

1. Upload contents of `dist/` folder to your web server
2. Configure your web server to serve `index.html` for all routes
3. Ensure proper MIME types are set

## Environment Variables

For production deployment, you may want to set these environment variables:

- `NODE_ENV=production`
- `PUBLIC_URL=https://yourdomain.com`

## Custom Domain

1. Purchase a domain (e.g., numeriquai.com)
2. Configure DNS settings according to your hosting provider
3. Update the meta tags in `src/index.html` with your domain
4. Set up SSL certificate (most platforms do this automatically)

## Performance Optimization

The build process already includes:
- CSS and JavaScript minification
- Asset optimization
- Code splitting
- Gzip compression ready

Additional optimizations:
- Enable Gzip compression on your server
- Set up CDN for static assets
- Configure browser caching headers

## Monitoring

After deployment:
1. Test all functionality
2. Check mobile responsiveness
3. Verify SEO meta tags
4. Test loading speed with tools like PageSpeed Insights
5. Set up analytics (Google Analytics, etc.)

## Troubleshooting

### Common Issues

1. **404 errors on refresh:** Configure your server to serve `index.html` for all routes
2. **Missing assets:** Ensure all files from `dist/` are uploaded
3. **CORS issues:** Configure proper headers on your server
4. **SSL issues:** Ensure HTTPS is properly configured

### Support

For deployment issues, contact: info@numeriquai.com 