# Domain Echo - Official Website

Modern promotional website for the Domain Echo Chrome extension, built with Astro and Tailwind CSS.

## 🚀 Pages

- **/** - Landing page with hero, features, how-it-works, install, and FAQ sections
- **/about** - About Domain Echo and our mission
- **/privacy** - Privacy Policy
- **/terms** - Terms of Service

## 🛠️ Tech Stack

- **Astro** - Fast, modern static site generator
- **Tailwind CSS** - Utility-first CSS framework
- **TypeScript** - Type-safe development

## 📦 Getting Started

### Install Dependencies

```bash
npm install
```

### Development Server

```bash
npm run dev
```

Visit `http://localhost:4321` to see the site.

### Build for Production

```bash
npm run build
```

The built site will be in the `dist/` folder.

### Preview Production Build

```bash
npm run preview
```

## 🚀 Deployment

### Option 1: Vercel (Recommended - FREE)

1. Install Vercel CLI:
   ```bash
   npm i -g vercel
   ```

2. Deploy:
   ```bash
   vercel
   ```

3. For production:
   ```bash
   vercel --prod
   ```

### Option 2: Netlify (FREE)

1. Install Netlify CLI:
   ```bash
   npm i -g netlify-cli
   ```

2. Deploy:
   ```bash
   netlify deploy
   ```

3. For production:
   ```bash
   netlify deploy --prod
   ```

### Option 3: Your VPS

1. Build the site:
   ```bash
   npm run build
   ```

2. Copy the `dist/` folder to your VPS:
   ```bash
   scp -r dist/* user@your-vps:/var/www/domainecho
   ```

3. Configure Nginx:
   ```nginx
   server {
       listen 80;
       server_name yourdomain.com;
       root /var/www/domainecho;
       index index.html;
       
       location / {
           try_files $uri $uri/ /index.html;
       }
   }
   ```

4. Restart Nginx:
   ```bash
   sudo systemctl restart nginx
   ```

### Option 4: GitHub Pages (FREE)

1. Build the site:
   ```bash
   npm run build
   ```

2. Push the `dist/` folder to a `gh-pages` branch
3. Enable GitHub Pages in your repo settings

## 📝 Customization

### Update Install Link

When your extension is published to the Chrome Web Store, update the install links in:
- `src/pages/index.astro` (search for `href="#"`)
- `src/layouts/Layout.astro` (navigation install button)

Replace `#` with your Chrome Web Store URL.

### Change Colors

Edit Tailwind colors in `tailwind.config.mjs` or use Tailwind's default color palette.

### Add Content

All pages are in `src/pages/`:
- `index.astro` - Home page
- `about.astro` - About page
- `privacy.astro` - Privacy policy
- `terms.astro` - Terms of service

The shared layout is in `src/layouts/Layout.astro`.

## 🎨 Design Features

- ✅ Fully responsive (mobile, tablet, desktop)
- ✅ Dark theme with indigo/purple accents
- ✅ Modern gradient effects
- ✅ Clean, minimal design
- ✅ Fast loading with Astro
- ✅ SEO-friendly
- ✅ Accessible

## 📊 Performance

Astro generates static HTML for blazing-fast performance:
- No JavaScript by default
- Optimized CSS
- Fast page loads
- Great Lighthouse scores

## 🔧 Project Structure

```
/
├── public/          # Static assets
├── src/
│   ├── layouts/     # Page layouts
│   │   └── Layout.astro
│   ├── pages/       # Pages (routes)
│   │   ├── index.astro
│   │   ├── about.astro
│   │   ├── privacy.astro
│   │   └── terms.astro
│   └── styles/      # Global styles
│       └── global.css
├── astro.config.mjs # Astro configuration
├── tailwind.config.mjs # Tailwind configuration
└── package.json
```

## 📄 License

Same as the Domain Echo extension.

# domain-echo-site
