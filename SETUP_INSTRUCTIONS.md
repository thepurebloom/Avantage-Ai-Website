# Project Setup Instructions

## Overview
This project uses Next.js with TypeScript, Tailwind CSS, and shadcn/ui components.

## Prerequisites
- Node.js 18+ installed
- npm or pnpm package manager

## Setup Steps

### 1. Initialize Next.js Project with TypeScript
```bash
npx create-next-app@latest . --typescript --tailwind --app --eslint --src-dir --import-alias "@/*"
```

When prompted, answer:
- ✔ Would you like to use TypeScript? **Yes**
- ✔ Would you like to use ESLint? **Yes**
- ✔ Would you like to use Tailwind CSS? **Yes**
- ✔ Would you like to use `src/` directory? **Yes**
- ✔ Would you like to use App Router? **Yes**
- ✔ Would you like to customize the default import alias? **No** (use @/*)

### 2. Initialize shadcn/ui
```bash
npx shadcn@latest init
```

When prompted, choose:
- ✔ Which style would you like to use? **Default**
- ✔ Which color would you like to use as base color? **Slate**
- ✔ Would you like to use CSS variables for colors? **Yes**

This will:
- Create `components.json` configuration file
- Set up the `components/ui` directory at `src/components/ui`
- Configure path aliases

### 3. Install Required Dependencies
```bash
npm install three gsap
npm install -D @types/three
```

### 4. Project Structure
After setup, your project structure will be:
```
/Users/meersheikh/Avantage Ai website/
├── src/
│   ├── app/
│   │   ├── layout.tsx
│   │   ├── page.tsx
│   │   └── globals.css
│   ├── components/
│   │   └── ui/
│   │       ├── horizon-hero-section.tsx
│   │       └── demo.tsx
│   └── lib/
│       └── utils.ts
├── public/
├── components.json
├── package.json
├── tsconfig.json
├── tailwind.config.ts
├── next.config.js
└── postcss.config.js
```

## Why `components/ui` Directory is Important

The `components/ui` directory is a shadcn convention that:

1. **Separates UI primitives from business logic** - All reusable UI components go here
2. **Enables CLI component installation** - shadcn CLI automatically adds components here
3. **Maintains consistency** - All team members know where to find UI components
4. **Supports customization** - You own the component code and can modify it
5. **Path aliasing** - Components are imported as `@/components/ui/component-name`

## Usage

After setup, you can use the component in any page:

```tsx
import { DemoOne } from "@/components/ui/demo";

export default function Home() {
  return (
    <main>
      <DemoOne />
    </main>
  );
}
```

## Development Server
```bash
npm run dev
```

Visit `http://localhost:3000` to see your application.

## Component Details

### Horizon Hero Section
- Uses Three.js for 3D space rendering
- GSAP for smooth scroll animations
- Responsive and performant
- Includes parallax mountains, stars, and nebula effects

### Required Assets
- None - all graphics are generated programmatically with Three.js

### External Dependencies
- `three` - 3D graphics library
- `gsap` - Animation library
- `@types/three` - TypeScript definitions

## Next Steps

1. Run the setup commands above
2. The component files are already created
3. Add the component to your main page
4. Customize the content and styling as needed

## Troubleshooting

### If you get "Cannot find module '@/components/ui/...'"
Check your `tsconfig.json` has the correct path mapping:
```json
{
  "compilerOptions": {
    "paths": {
      "@/*": ["./src/*"]
    }
  }
}
```

### If Three.js types are not recognized
Install the types package:
```bash
npm install -D @types/three
```

### If GSAP ScrollTrigger doesn't work
Make sure you're registering the plugin:
```tsx
import { gsap } from 'gsap';
import { ScrollTrigger } from 'gsap/ScrollTrigger';
gsap.registerPlugin(ScrollTrigger);
```


