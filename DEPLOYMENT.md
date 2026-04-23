# 🚀 DEPLOYMENT GUIDE - BabyBee Portfolio

## FASTEST DEPLOYMENT (5 minutes)

### ✅ Vercel (RECOMMENDED)

**Why Vercel?**
- Free hosting
- Automatic HTTPS
- Global CDN
- Zero configuration
- Custom domain support

**Steps:**

1. **Create GitHub Repository**
   - Go to github.com
   - Create new repository "babybee-portfolio"
   - Don't initialize with README

2. **Push Your Code**
   ```bash
   cd babybee-portfolio
   git init
   git add .
   git commit -m "Initial commit"
   git remote add origin https://github.com/YOUR_USERNAME/babybee-portfolio.git
   git push -u origin main
   ```

3. **Deploy to Vercel**
   - Go to vercel.com
   - Sign in with GitHub
   - Click "New Project"
   - Import your repository
   - Click "Deploy" (Vercel auto-detects Vite)
   - Done! Your site is live

4. **Custom Domain (Optional)**
   - In Vercel dashboard, go to Settings → Domains
   - Add your domain (e.g., babybee.com)
   - Update DNS records as instructed
   - HTTPS is automatic

---

## ALTERNATIVE OPTIONS

### 🟢 Netlify

```bash
# 1. Build your site
npm run build

# 2. Install Netlify CLI
npm install -g netlify-cli

# 3. Deploy
netlify deploy --prod --dir=dist
```

OR use Netlify's drag-and-drop:
1. Build: `npm run build`
2. Go to netlify.com
3. Drag the `dist` folder to the upload area

---

### 🟠 Traditional Hosting (cPanel, Shared Hosting)

**For: HostGator, Bluehost, GoDaddy, etc.**

1. **Build the site:**
   ```bash
   npm run build
   ```

2. **Upload files:**
   - Open your hosting File Manager or FTP
   - Navigate to `public_html` (or your domain folder)
   - Upload EVERYTHING from the `dist` folder
   - Do NOT upload the dist folder itself, just its contents

3. **Set up domain:**
   - Point your domain to the uploaded files
   - Wait for DNS propagation (up to 24 hours)

---

### 🔵 GitHub Pages (Free)

1. **Install gh-pages:**
   ```bash
   npm install --save-dev gh-pages
   ```

2. **Update package.json:**
   Add this to the scripts section:
   ```json
   "homepage": "https://YOUR_USERNAME.github.io/babybee-portfolio",
   "predeploy": "npm run build",
   "deploy": "gh-pages -d dist"
   ```

3. **Deploy:**
   ```bash
   npm run deploy
   ```

4. **Enable GitHub Pages:**
   - Go to repository Settings → Pages
   - Source: gh-pages branch
   - Your site will be live at the homepage URL

---

## CUSTOM DOMAIN SETUP

### For Vercel/Netlify:
1. Add domain in dashboard
2. Update DNS records:
   - A record: Point to their IP
   - CNAME record: www → your-app.vercel.app

### For Traditional Hosting:
1. Point nameservers to your host
2. Update A record to host IP
3. Wait for DNS propagation

---

## TROUBLESHOOTING

**Build fails?**
- Delete `node_modules` and `package-lock.json`
- Run `npm install` again
- Run `npm run build`

**Page not loading?**
- Check if files are in the root directory (not in a subfolder)
- Clear browser cache
- Check hosting server logs

**Styling broken?**
- Ensure all files from `dist` folder are uploaded
- Check if CSS/JS files are loading in browser console

**Contact forms not working?**
- Set up backend API or use services like:
  - Formspree
  - EmailJS
  - Netlify Forms (if using Netlify)

---

## ONGOING UPDATES

**To update your live site:**

1. Make changes in `src/BabyBeePortfolio.jsx`
2. Test locally: `npm run dev`
3. Push to GitHub:
   ```bash
   git add .
   git commit -m "Update content"
   git push
   ```
4. Vercel/Netlify will auto-deploy
5. For traditional hosting, rebuild and re-upload dist folder

---

## PERFORMANCE OPTIMIZATION

After deployment:
- Test site speed: pagespeed.web.dev
- Optimize images (use WebP format)
- Enable compression on server
- Use CDN for video files

---

## NEED HELP?

Contact BabyBee Studios or check:
- Vercel Docs: vercel.com/docs
- Netlify Docs: docs.netlify.com
- Vite Docs: vitejs.dev
