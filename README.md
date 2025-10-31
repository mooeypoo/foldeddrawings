# FoldedDrawings Website

A beautiful, static website for the FoldedDrawings Etsy shop featuring printable PDF coloring pages.

## 🚀 Quick Start

```bash
# Install dependencies
npm install

# Start development server
npm run dev

# Build for production
npm run build

# Preview production build
npm preview
```

## 📁 Project Structure

```
foldeddrawings/
├── src/
│   ├── components/          # Reusable Astro/Vue components
│   │   ├── FeaturedPdfCard.astro
│   │   ├── Nav.astro
│   │   └── TutorialCard.astro
│   ├── data/                # JSON configuration files (easy to update!)
│   │   ├── featured-pdfs.json
│   │   ├── site-config.json
│   │   └── tutorials.json
│   ├── layouts/             # Page layouts
│   │   └── BaseLayout.astro
│   ├── pages/               # Route pages
│   │   ├── index.astro     # Landing page
│   │   └── contact.astro   # Contact page
│   └── styles/
│       └── global.css       # Tailwind CSS imports
└── public/                  # Static assets
```

## ✏️ Easy Updates

### Adding/Removing Featured PDFs

Edit `src/data/featured-pdfs.json`:

```json
{
  "id": "5",
  "title": "New Design",
  "description": "Description here",
  "image": "https://your-image-url.jpg",
  "etsyUrl": "https://www.etsy.com/your-listing",
  "price": "$4.99",
  "featured": true
}
```

Set `"featured": false` to hide a PDF, or remove it entirely.

### Updating Tutorials

Edit `src/data/tutorials.json`:

```json
{
  "id": "4",
  "title": "New Tutorial",
  "description": "Tutorial description",
  "youtubeId": "YOUTUBE_VIDEO_ID"
}
```

### Updating Site Information

Edit `src/data/site-config.json` to change:
- Shop name and tagline
- Etsy shop URL
- Contact email
- Site metadata

## 🎨 Customization

### Colors & Styling

The site uses Tailwind CSS with a purple/pink gradient theme. To change colors, update the gradient classes in:
- `src/components/Nav.astro`
- `src/layouts/BaseLayout.astro`
- `src/pages/index.astro`

Look for classes like `from-purple-600 to-pink-600` and modify as needed.

### Images

Replace placeholder images in `featured-pdfs.json` with actual product images. You can:
- Host images in the `public/` folder
- Use a CDN or image hosting service
- Link directly to Etsy listing images

## 📧 Contact Form Setup

The contact form uses **Netlify Forms**, which is automatically configured when deployed to Netlify. The form includes:

- **Automatic email delivery** to `info@FoldedDrawings.com` (configured in Netlify dashboard)
- **Spam protection** via honeypot field
- **Success/error messaging** with user feedback

### Netlify Forms Configuration

1. **Form Detection**: Netlify automatically detects forms during build (see `public/netlify-forms.html`)
2. **Email Notifications**: 
   - Go to your Netlify site dashboard
   - Navigate to Forms → Form notifications
   - Add email notification to `info@FoldedDrawings.com`
3. **Form Submissions**: View all submissions in Netlify dashboard under Forms

No additional setup needed - it works automatically when deployed to Netlify!

## 🚢 Deployment to Netlify

This site is configured for **Netlify** deployment with automatic form handling.

### Quick Deploy (Recommended)

1. **Push to GitHub**:
   ```bash
   git add .
   git commit -m "Initial commit"
   git push origin main
   ```

2. **Connect to Netlify**:
   - Go to [app.netlify.com](https://app.netlify.com)
   - Click "Add new site" → "Import an existing project"
   - Connect your GitHub repository
   - Netlify will auto-detect settings from `netlify.toml`

3. **Configure Email Notifications**:
   - In Netlify dashboard, go to **Forms**
   - Find your "contact" form
   - Click **Notifications & webhooks**
   - Add email notification to `info@FoldedDrawings.com`

That's it! Your site will automatically deploy on every push to `main`.

### Manual Deploy

```bash
npm run build
# Then drag the `dist/` folder to Netlify drop zone
```

### Other Hosting Options

- **Vercel**: Similar setup, uses serverless functions for forms
- **GitHub Pages**: Manual form setup required (use Formspree or EmailJS)
- **Cloudflare Pages**: Similar to Netlify

## 🛠️ Tech Stack

- **Astro**: Static site generator
- **Vue.js**: Component framework (integrated)
- **Tailwind CSS**: Utility-first CSS framework
- **TypeScript**: Type-safe development

## 📝 Notes

- All featured PDFs must have `"featured": true` to appear on the landing page
- YouTube video IDs are extracted from URLs: `youtube.com/watch?v=VIDEO_ID`
- The site is fully responsive and works on mobile, tablet, and desktop
- All Etsy links open in a new tab for better UX

## 🎯 Architecture Benefits

- **Data-Driven**: Update content via JSON files, no code changes needed
- **Component-Based**: Reusable components for consistent design
- **Static Generation**: Fast loading times and great SEO
- **Easy Maintenance**: Clear separation of content, components, and styles