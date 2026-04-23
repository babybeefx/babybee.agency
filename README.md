# BabyBee Portfolio Website

Professional portfolio website for BabyBee - a video editing agency based in Bangladesh.

## 🚀 Quick Start

### Prerequisites
- Node.js 18+ installed
- npm or yarn package manager

### Installation

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

## 📦 Deployment Options

### Option 1: Vercel (Recommended)
1. Push code to GitHub
2. Go to [vercel.com](https://vercel.com)
3. Import your repository
4. Deploy (automatic setup for Vite projects)

### Option 2: Netlify
1. Push code to GitHub
2. Go to [netlify.com](https://netlify.com)
3. "Add new site" → "Import from Git"
4. Build command: `npm run build`
5. Publish directory: `dist`

### Option 3: GitHub Pages
```bash
# Install gh-pages
npm install --save-dev gh-pages

# Add to package.json scripts:
"deploy": "vite build && gh-pages -d dist"

# Deploy
npm run deploy
```

### Option 4: Traditional Hosting (cPanel/Shared)
1. Run `npm run build`
2. Upload everything from the `dist` folder to your web host
3. Point your domain to the uploaded files

## 🛠️ Tech Stack

- **React 18** - UI framework
- **Vite** - Build tool
- **Tailwind CSS** - Styling
- **Google Fonts** - Inter & Hind Siliguri

## 📁 Project Structure

```
babybee-portfolio/
├── src/
│   ├── BabyBeePortfolio.jsx  # Main component
│   ├── main.jsx               # Entry point
│   └── index.css              # Global styles
├── index.html                 # HTML template
├── package.json               # Dependencies
├── vite.config.js            # Vite configuration
├── tailwind.config.js        # Tailwind configuration
└── postcss.config.js         # PostCSS configuration
```

## ✨ Features

- **Responsive Design** - Works on all devices
- **Smooth Scroll** - Navigation with scroll spy
- **Portfolio Tabs** - Long-form & short-form video sections
- **Team Section** - With birthday notifications
- **Dark Theme** - Modern glassmorphism design
- **Performance** - Optimized with Vite

## 🎨 Customization

### Update Content
Edit `src/BabyBeePortfolio.jsx`:
- Portfolio items (lines 13-36)
- Team members (lines 39-45)
- Services (line 166+)
- Contact links (lines 281-284)

### Update Styling
- Colors: Search for `#FFA500` (orange accent)
- Fonts: Modify `tailwind.config.js`
- Layout: All in `BabyBeePortfolio.jsx`

## 📞 Support

For issues or questions, contact BabyBee Studios.

---

Built with ❤️ by BabyBee Studios
