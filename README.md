# Avantage AI Website

A stunning Next.js website featuring an immersive Three.js hero section with GSAP scroll animations.

## 🚀 Features

- **Next.js 14** with App Router
- **TypeScript** for type safety
- **Tailwind CSS** for styling
- **shadcn/ui** component system
- **Three.js** for 3D graphics and space visualization
- **GSAP** for smooth scroll animations
- Fully responsive design
- Optimized performance

## 🎨 Hero Section

The Horizon Hero Section features:
- 3D star field with 5000+ animated stars
- Dynamic nebula with shader effects
- Parallax mountain layers
- Atmospheric glow effects
- Smooth scroll-based camera transitions
- Progressive content reveals through 3 sections:
  1. **HORIZON** - Where vision meets reality
  2. **COSMOS** - Beyond the boundaries of imagination
  3. **INFINITY** - The essence of true innovation

## 📋 Prerequisites

- Node.js 18 or higher
- npm or pnpm package manager

## 🛠️ Installation

1. **Install dependencies:**

```bash
npm install
```

This will install all required packages including:
- `next`, `react`, `react-dom`
- `three` and `@types/three`
- `gsap`
- `tailwindcss` and utilities
- `shadcn/ui` dependencies

2. **Run the development server:**

```bash
npm run dev
```

3. **Open your browser:**

Navigate to [http://localhost:3000](http://localhost:3000)

## 📁 Project Structure

```
/Users/meersheikh/Avantage Ai website/
├── src/
│   ├── app/
│   │   ├── layout.tsx          # Root layout
│   │   ├── page.tsx            # Home page
│   │   └── globals.css         # Global styles + Hero styles
│   ├── components/
│   │   └── ui/
│   │       ├── horizon-hero-section.tsx  # Main hero component
│   │       └── demo.tsx                  # Demo wrapper
│   └── lib/
│       └── utils.ts            # Utility functions
├── public/                     # Static assets
├── components.json             # shadcn/ui config
├── package.json
├── tsconfig.json
├── tailwind.config.ts
└── next.config.js
```

## 🎯 Usage

### Using the Hero Component

The hero component is already integrated into the home page. To use it elsewhere:

```tsx
import { DemoOne } from "@/components/ui/demo";

export default function YourPage() {
  return (
    <main>
      <DemoOne />
    </main>
  );
}
```

### Customizing Content

Edit the sections in `src/components/ui/horizon-hero-section.tsx`:

```tsx
const titles = {
  0: 'HORIZON',
  1: 'YOUR TITLE',
  2: 'ANOTHER TITLE'
};

const subtitles = {
  0: {
    line1: 'Your first line,',
    line2: 'Your second line'
  },
  // ... more sections
};
```

### Styling

All hero-specific styles are in `src/app/globals.css`. The component uses:
- CSS custom properties for theming
- Tailwind utility classes
- Custom animations for scroll effects

## 🎨 Customization

### Colors

Modify the nebula and atmosphere colors in the component:

```tsx
// Nebula colors
color1: { value: new THREE.Color(0x0033ff) },  // Blue
color2: { value: new THREE.Color(0xff0066) },  // Pink

// Atmosphere color
vec3 atmosphere = vec3(0.3, 0.6, 1.0) * intensity;
```

### Animation Speed

Adjust scroll animation speeds:

```tsx
// Camera smoothing (lower = smoother)
const smoothingFactor = 0.05;

// Star rotation speed
float angle = time * 0.05 * (1.0 - depth * 0.3);
```

### Number of Sections

Change `totalSections` in the component:

```tsx
const totalSections = 3; // Adjust as needed
```

## 🏗️ Building for Production

```bash
npm run build
npm start
```

## 📦 Dependencies

### Core Dependencies
- `next` - React framework
- `react` & `react-dom` - React library
- `three` - 3D graphics library
- `gsap` - Animation library
- `tailwindcss` - Utility-first CSS

### shadcn/ui Dependencies
- `class-variance-authority` - Component variants
- `clsx` - Conditional classes
- `tailwind-merge` - Merge Tailwind classes
- `lucide-react` - Icon library

### Dev Dependencies
- `typescript` - Type checking
- `@types/three` - Three.js types
- `@types/react` - React types
- `eslint` - Code linting

## 🌐 Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)

**Note:** Three.js requires WebGL support.

## 🚀 Performance Tips

1. The component is already optimized for performance
2. Star count can be reduced for mobile devices
3. Post-processing effects can be disabled on low-end devices
4. Uses `requestAnimationFrame` for smooth animations
5. Proper cleanup prevents memory leaks

## 🐛 Troubleshooting

### Component not rendering
- Ensure `"use client"` is at the top of the component file
- Check browser console for WebGL errors
- Verify Three.js and GSAP are installed

### TypeScript errors
- Run `npm install @types/three`
- Check `tsconfig.json` paths are correct

### Scroll not working
- Ensure the container has sufficient height
- Check that GSAP ScrollTrigger is registered

## 📄 License

This project is part of Avantage AI's website.

## 🤝 Contributing

For questions or contributions, please contact the Avantage AI team.

---

Built with ❤️ using Next.js, Three.js, and GSAP


