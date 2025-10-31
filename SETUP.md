# Quick Setup Guide

## Getting Started

1. **Install dependencies** (if not already done):
   ```bash
   npm install
   ```

2. **Start development server**:
   ```bash
   npm run dev
   ```
   Visit `http://localhost:4321` to see your site!

## Making Updates

### Update Featured PDFs

Edit `src/data/featured-pdfs.json`:
- Add new PDFs by copying an existing entry
- Set `"featured": true` to show on homepage
- Replace placeholder images with real product images
- Update Etsy URLs with your actual listings

### Update Tutorials

Edit `src/data/tutorials.json`:
- Add YouTube video IDs (the part after `v=` in YouTube URLs)
- Update titles and descriptions

### Update Site Info

Edit `src/data/site-config.json`:
- Change shop name, tagline, URLs
- Update contact email

### Change Design Colors

The site uses purple/pink gradients. To change colors, search for:
- `purple-600` / `pink-600` in component files
- Replace with your preferred Tailwind color classes

## Contact Form Setup

The contact form is **already configured** to use Netlify Forms! No setup needed.

### Configure Email Notifications

1. Deploy your site to Netlify (see Deployment section)
2. In Netlify dashboard, go to **Forms** → **Form notifications**
3. Add email notification to: `info@FoldedDrawings.com`
4. All form submissions will be sent to this email automatically

The form includes:
- ✅ Automatic spam protection (honeypot field)
- ✅ Success/error messaging
- ✅ Form submission tracking in Netlify dashboard

## Deployment to Netlify

### Method 1: Git Integration (Recommended)

1. **Push your code to GitHub**:
   ```bash
   git add .
   git commit -m "Ready to deploy"
   git push origin main
   ```

2. **Connect to Netlify**:
   - Visit [app.netlify.com](https://app.netlify.com)
   - Click "Add new site" → "Import an existing project"
   - Select your GitHub repository
   - Netlify will auto-detect build settings from `netlify.toml`
   - Click "Deploy site"

3. **Configure Email Notifications**:
   - After first deployment, go to **Forms** in Netlify dashboard
   - Click on your contact form → **Notifications & webhooks**
   - Add email notification to `info@FoldedDrawings.com`

Your site will now automatically deploy on every push!

### Method 2: Manual Deploy

1. Build the site: `npm run build`
2. Go to Netlify dashboard
3. Drag and drop the `dist/` folder
4. Configure email notifications as above

The `netlify.toml` file is already configured with the correct build settings.

## Framework Choice: Why Astro?

✅ **Perfect for static sites** - Generates fast, optimized HTML
✅ **Vue.js support** - Can use Vue components when needed
✅ **Easy content management** - JSON files for easy updates
✅ **Great performance** - Minimal JavaScript, fast load times
✅ **SEO-friendly** - Server-rendered HTML by default
✅ **Simple architecture** - Easy to understand and maintain

## Architecture Benefits

- **Data-driven**: Update content without touching code
- **Component-based**: Reusable, maintainable components
- **Type-safe**: TypeScript for fewer errors
- **Modern stack**: Tailwind CSS for quick styling
- **Scalable**: Easy to add new pages and features

## Next Steps

1. Replace placeholder images with actual product photos
2. Update YouTube video IDs with your tutorial videos
3. Set up contact form with your preferred service
4. Update Etsy shop URLs
5. Deploy and share your site!

For more details, see the main [README.md](./README.md).
