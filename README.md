# Numeriquai Website

A professional coming soon website for Numeriquai - Reliable AI Foundational Models.

## Features

- 🎨 Modern, responsive design with Bootstrap 5
- 📱 Mobile-first approach
- ⚡ Fast loading with webpack optimization
- 🔍 SEO optimized with proper meta tags
- 📧 Newsletter signup functionality
- 🎭 Smooth animations and transitions
- 🎯 Professional coming soon page

## Tech Stack

- **Frontend Framework**: Bootstrap 5
- **Build Tool**: Webpack 5
- **CSS Preprocessor**: Sass
- **JavaScript**: ES6+ with Babel
- **Icons**: Bootstrap Icons
- **Development Server**: Webpack Dev Server

## Project Structure

```
numeriquai-fe/
├── src/
│   ├── index.html          # Main HTML template
│   ├── js/
│   │   └── main.js         # Main JavaScript entry point
│   └── scss/
│       └── main.scss       # Main stylesheet
├── dist/                   # Build output (generated)
├── package.json           # Dependencies and scripts
├── webpack.config.js      # Webpack configuration
└── README.md              # This file
```

## Getting Started

### Prerequisites

- Node.js (version 14 or higher)
- npm or yarn

### Installation

1. Clone the repository:
```bash
git clone <repository-url>
cd numeriquai-fe
```

2. Install dependencies:
```bash
npm install
```

### Development

Start the development server:
```bash
npm run dev
```

This will:
- Start a development server at `http://localhost:3000`
- Enable hot reloading
- Open the browser automatically

### Building for Production

Build the project for production:
```bash
npm run build
```

This will:
- Create optimized files in the `dist/` directory
- Minify CSS and JavaScript
- Generate hashed filenames for caching

### Available Scripts

- `npm run dev` - Start development server
- `npm run build` - Build for production
- `npm run start` - Start development server and open browser

## Customization

### Colors and Branding

The website uses CSS custom properties for easy customization. Edit the variables in `src/scss/main.scss`:

```scss
:root {
    --primary-color: #0d6efd;
    --secondary-color: #6c757d;
    --accent-color: #6610f2;
    // ... more variables
}
```

### Content

- Update the main content in `src/index.html`
- Modify the coming soon message and features
- Update contact information and social links

### SEO

The HTML template includes comprehensive SEO meta tags. Update them in `src/index.html`:

- Page title
- Meta description
- Open Graph tags
- Twitter Card tags

## Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)
- Mobile browsers

## Performance

The build process includes several optimizations:

- CSS and JavaScript minification
- Asset optimization
- Code splitting
- Tree shaking
- Gzip compression ready

## Deployment

The `dist/` folder contains the production-ready files that can be deployed to any static hosting service:

- Netlify
- Vercel
- GitHub Pages
- AWS S3
- Any web server

### GitHub Pages Deployment

This project includes automated CI/CD with GitHub Actions for deployment to GitHub Pages.

#### Setup Steps (One-time):

1. **Enable GitHub Pages**:
   - Go to your repository on GitHub
   - Navigate to **Settings** → **Pages**
   - Under "Source", select **"GitHub Actions"**
   - Save the settings

2. **Verify Repository Settings**:
   - Ensure your repository is public (or you have GitHub Pro for private repos)
   - Make sure the main branch is named `main` (not `master`)

#### Automated Deployment:

- **Every push to `main` branch** will automatically trigger a build and deployment
- **Pull requests** will trigger a build for testing (but won't deploy)
- The site will be available at: `https://<your-username>.github.io/<repository-name>/`

#### Manual Deployment:

If you need to manually trigger a deployment:
1. Go to **Actions** tab in your repository
2. Select the "Deploy to GitHub Pages" workflow
3. Click **"Run workflow"**
4. Select the branch and click **"Run workflow"**

#### Deployment Status:

- Check the **Actions** tab to monitor build and deployment progress
- Successful deployments will show a green checkmark
- Failed deployments will show detailed error logs

## Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Test thoroughly
5. Submit a pull request

## License

This project is licensed under the MIT License.

## Contact

For questions or support, contact: info@numeriquai.com 