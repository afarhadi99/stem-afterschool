# 🚀 Aura City - Deployment Guide

Complete guide to deploy your Aura City website to GitHub and Vercel.

## 📋 Prerequisites

- GitHub account (free at https://github.com)
- Vercel account (free at https://vercel.com)
- Git installed on your computer

## 🔧 Step 1: Set Up GitHub Repository

### 1.1 Create a New Repository

1. Go to [GitHub](https://github.com) and log in
2. Click the **+** icon in the top right → **New repository**
3. Fill in the details:
   - **Repository name**: `aura-city-website`
   - **Description**: `Luxury tech-enabled fashion e-commerce website`
   - **Public** (so Vercel can access it)
   - **Initialize with README**: Uncheck (we have our own)
4. Click **Create repository**

### 1.2 Clone and Push Your Code

```bash
# Clone the repository
git clone https://github.com/YOUR_USERNAME/aura-city-website.git
cd aura-city-website

# Extract the zip file contents into this directory
# (Copy all files from the zip into the cloned folder)

# Initialize git and push
git add .
git commit -m "Initial commit: Aura City website with all assets"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/aura-city-website.git
git push -u origin main
```

**Replace `YOUR_USERNAME` with your actual GitHub username**

## 🌐 Step 2: Deploy to Vercel

### 2.1 Connect Vercel to GitHub

1. Go to [Vercel](https://vercel.com) and sign up/log in
2. Click **New Project**
3. Click **Import Git Repository**
4. Authorize Vercel to access your GitHub account
5. Select `aura-city-website` repository

### 2.2 Configure Project Settings

1. **Project Name**: `aura-city-website` (or your preferred name)
2. **Framework Preset**: Select **Other** (it's a static site)
3. **Root Directory**: Leave as `.`
4. **Build Command**: Leave empty
5. **Output Directory**: Leave empty
6. Click **Deploy**

### 2.3 Wait for Deployment

Vercel will automatically:
- Build your site
- Deploy to a live URL
- Provide you with a unique domain (e.g., `aura-city-website.vercel.app`)

## ✅ Verification

After deployment, verify everything works:

1. **Visit your live site**: Click the URL provided by Vercel
2. **Test the cart**: Add items and verify toast notifications
3. **Check responsiveness**: Test on mobile devices
4. **Verify images**: All 24 product images should load
5. **Test navigation**: Click through all sections

## 🔄 Making Updates

After deployment, any changes you push to GitHub will automatically redeploy:

```bash
# Make changes to your files
# Then:
git add .
git commit -m "Update: [describe your changes]"
git push origin main

# Vercel will automatically redeploy!
```

## 🎯 Custom Domain (Optional)

To use your own domain:

1. In Vercel dashboard, go to **Settings** → **Domains**
2. Add your custom domain
3. Follow the DNS configuration instructions
4. Wait for DNS propagation (usually 24-48 hours)

## 📊 Performance Tips

- All images are optimized and compressed
- Static site loads instantly
- No build process needed
- Vercel provides global CDN for fast delivery

## 🆘 Troubleshooting

### Images not loading
- Ensure all `generated_image_*.png` files are in the root directory
- Check file names match exactly in `index.html`

### Cart not working
- Open browser console (F12) and check for JavaScript errors
- Ensure JavaScript is enabled

### Deployment failed
- Check that all files are in the repository
- Verify `.gitignore` isn't excluding important files
- Check Vercel deployment logs for errors

## 📞 Support

- **Vercel Docs**: https://vercel.com/docs
- **GitHub Help**: https://docs.github.com
- **Aura City Email**: hello@auracity.com

## 🎉 You're Live!

Your Aura City website is now live on the internet! Share your URL with the world.

---

**Pro Tips:**
- Enable Vercel Analytics to track visitors
- Set up automatic deployments for every push
- Use Vercel's built-in SEO tools
- Monitor performance with Vercel's dashboard
