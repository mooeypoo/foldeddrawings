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

**Option 1: Formspree (Recommended)**
1. Go to https://formspree.io and sign up
2. Create a new form
3. Copy your form ID
4. In `src/pages/contact.astro`, replace `your-form-id` with your actual form ID

**Option 2: EmailJS**
1. Sign up at https://www.emailjs.com
2. Follow their Vue.js integration guide
3. Replace the form action with EmailJS

**Option 3: Netlify Forms** (if deploying to Netlify)
1. Add `netlify` attribute to the form
2. Netlify will automatically handle submissions

## Deployment

The site builds to the `dist/` folder. Deploy this folder to:
- **Netlify**: Connect your Git repo → automatic deployments
- **Vercel**: Connect your Git repo → automatic deployments  
- **GitHub Pages**: Use GitHub Actions or manually upload `dist/`
- **Cloudflare Pages**: Connect Git repo → automatic deployments

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
