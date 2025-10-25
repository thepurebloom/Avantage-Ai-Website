# 🚀 Quick Start Guide

Get your Avantage AI website running in 3 steps!

## Step 1: Install Dependencies

```bash
npm install
```

This installs everything you need:
- Next.js, React, TypeScript
- Three.js for 3D graphics
- GSAP for animations
- Tailwind CSS for styling
- shadcn/ui components

## Step 2: Start Development Server

```bash
npm run dev
```

## Step 3: View Your Site

Open [http://localhost:3000](http://localhost:3000) in your browser.

You should see the stunning Horizon hero section with:
- ⭐ Animated star field
- 🌌 Dynamic nebula effects
- 🏔️ Parallax mountains
- 📜 Smooth scroll animations

---

## 🎯 What's Included

✅ **Fully configured Next.js project** with TypeScript  
✅ **Tailwind CSS** with custom theme  
✅ **shadcn/ui** component system  
✅ **Three.js Horizon Hero Section** - production ready  
✅ **Responsive design** - works on all devices  
✅ **Performance optimized** - WebGL + GSAP  

---

## 📝 Next Steps

### Customize the Content

Edit `src/components/ui/horizon-hero-section.tsx` to change:
- Section titles (HORIZON, COSMOS, INFINITY)
- Subtitle text
- Number of scroll sections
- Colors and animations

### Add More Pages

Create new pages in `src/app/`:

```bash
src/app/about/page.tsx
src/app/services/page.tsx
src/app/contact/page.tsx
```

### Add shadcn Components

Install additional components as needed:

```bash
npx shadcn@latest add button
npx shadcn@latest add card
npx shadcn@latest add dialog
```

### Deploy to Production

Build and start production server:

```bash
npm run build
npm start
```

Or deploy to Vercel (recommended for Next.js):

```bash
# Install Vercel CLI
npm i -g vercel

# Deploy
vercel
```

---

## 🆘 Need Help?

Check out these files:
- `README.md` - Full documentation
- `SETUP_INSTRUCTIONS.md` - Detailed setup guide
- `src/components/ui/horizon-hero-section.tsx` - Component code with comments

---

## 🎨 Key Features to Explore

1. **Scroll Animation** - Scroll down to see the camera move through space
2. **Parallax Effect** - Mountains move at different speeds
3. **Star Rotation** - Stars slowly rotate around you
4. **Color Transitions** - Nebula colors animate smoothly
5. **Responsive UI** - Resize the window to see adaptive layout

---

**Tip:** Open browser DevTools (F12) and check the Performance tab while scrolling to see the optimized rendering!

---

Happy coding! 🚀✨
