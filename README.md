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

The contact form currently uses Formspree. To enable it:

1. Sign up at [formspree.io](https://formspree.io)
2. Create a new form
3. Replace `your-form-id` in `src/pages/contact.astro` with your Formspree form ID

Alternatively, you can use:
- **EmailJS**: For client-side email sending
- **Netlify Forms**: If deploying to Netlify
- **Vercel**: Serverless functions for form handling

## 🚢 Deployment

This is a static site that can be deployed to:

- **Netlify**: Connect your Git repo and deploy automatically
- **Vercel**: Similar to Netlify, great DX
- **GitHub Pages**: Free hosting for static sites
- **Cloudflare Pages**: Fast and reliable

Deploy commands:
```bash
npm run build
# Upload the `dist/` folder to your hosting provider
```

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