# QR Microsite Builder - Frontend# QR Microsite Builder - Frontend



A modern, drag-and-drop microsite builder with QR code generation capabilities. Create beautiful, mobile-responsive landing pages with 30+ customizable content blocks.> A drag-and-drop website builder for creating mobile-first microsites accessible via QR codes.



![React](https://img.shields.io/badge/React-18-blue)![Week 1 Status](https://img.shields.io/badge/Week%201-Complete-brightgreen)

![TypeScript](https://img.shields.io/badge/TypeScript-5-blue)![React](https://img.shields.io/badge/React-18-blue)

![Vite](https://img.shields.io/badge/Vite-5-purple)![TypeScript](https://img.shields.io/badge/TypeScript-5-blue)

![Tailwind CSS](https://img.shields.io/badge/Tailwind-3-cyan)![TailwindCSS](https://img.shields.io/badge/TailwindCSS-4-blue)



## ✨ Features## �� Quick Start



### 🎨 Visual Editor```bash

- **Drag & Drop Interface** - Intuitive block-based editor with real-time preview# Install dependencies

- **30+ Content Blocks** - Profile, links, hero, pricing, gallery, testimonials, and morenpm install

- **Live Device Preview** - Test your microsite on 20+ device sizes (iPhone, iPad, Desktop)

- **Theme Gallery** - 15+ professional themes with full customization# Start development server

- **AI Assistant** - Generate content and get design recommendationsnpm run dev



### 📱 Linktree-Style Features# Open in browser

- **Profile Block** - Avatar, bio, location, and social linkshttp://localhost:5173/editor/new

- **Link Buttons** - Beautiful, clickable buttons with icons and descriptions```

- **Social Links Grid** - Connect all your social media profiles

- **Payment Integration** - Accept payments via Stripe (Artist block)## 📦 Tech Stack



### 🎯 Professional Blocks- **Framework**: React 18 + TypeScript

- **Hero Sections** - Eye-catching headers with CTAs- **Build Tool**: Vite 7

- **Pricing Tables** - Feature comparison for products/services- **Styling**: TailwindCSS v4 + Shadcn UI

- **Testimonials** - Customer reviews with ratings- **Icons**: Lucide React

- **Gallery & Carousel** - Image slideshows with autoplay- **Animations**: Framer Motion

- **FAQ Accordion** - Collapsible Q&A sections- **Drag & Drop**: @dnd-kit

- **Stats Counter** - Animated statistics display- **Routing**: React Router v6

- **Maps Integration** - Embedded location maps- **ID Generation**: nanoid

- **Countdown Timers** - Event countdowns

- **Calendar** - Event listings with dates## ✨ Features (Week 1)



### 📊 Analytics & Insights### 🎨 Three-Panel Editor

- **Real-time Analytics** - Track views, clicks, and conversions- **Left Panel**: Draggable block palette

- **Geographic Data** - Visitor location heatmaps- **Center Panel**: Live canvas preview (mobile-first)

- **Device Analytics** - Desktop vs mobile breakdown- **Right Panel**: Block inspector with real-time editing

- **UTM Builder** - Campaign tracking tools

- **Export Reports** - Download analytics data### 🧱 Block Types

1. **Heading** - H1/H2/H3 with customizable text

### 🛠️ Advanced Features2. **Text** - Multi-line text content

- **Multi-tenancy Support** - Agency and team management3. **Button** - Call-to-action with URL

- **Custom Domains** - Use your own domain name4. **Image** - Upload or paste URL

- **A/B Testing** - Experiment with different designs5. **Spacer** - Adjustable vertical spacing

- **Tracking Pixels** - Facebook, Google Analytics integration6. **Form** - Coming in Week 2

- **Accessibility** - WCAG 2.1 compliant with keyboard navigation

- **Responsive Design** - Mobile-first, works on all devices### 🎯 Core Functionality

- ✅ Drag blocks from palette to canvas

## 🚀 Tech Stack- ✅ Reorder blocks via drag & drop

- ✅ Real-time block editing

- **Framework**: React 18 with TypeScript- ✅ Image upload (base64) + URL support

- **Build Tool**: Vite 5- ✅ Delete blocks

- **Styling**: Tailwind CSS + shadcn/ui components- ✅ Block selection

- **Animations**: Framer Motion- ✅ Live preview

- **Drag & Drop**: DnD Kit

- **State Management**: Zustand## 📂 Project Structure

- **Rich Text**: Tiptap editor

- **Charts**: Chart.js```

- **Routing**: React Router v6src/

├── components/

## 📋 Prerequisites│   ├── ui/              # Shadcn UI components

│   ├── editor/          # Editor-specific components

- Node.js 18+ │   │   ├── EditorLayout.tsx

- npm or yarn│   │   ├── BlockPalette.tsx

- Backend API running (see [qr-backend](https://github.com/Scanly-io/qr-backend))│   │   ├── Canvas.tsx

│   │   └── BlockInspector.tsx

## 🔧 Installation│   └── blocks/          # Block components (Week 2+)

├── pages/

1. **Clone the repository**│   ├── LoginPage.tsx

```bash│   ├── DashboardPage.tsx

git clone https://github.com/sbansa1/qr-frontend.git│   └── EditorPage.tsx

cd qr-frontend├── hooks/               # Custom React hooks

```├── types/               # TypeScript definitions

├── store/               # State management (Week 3+)

2. **Install dependencies**├── services/            # API services (Week 3+)

```bash└── lib/                 # Utilities

npm install```

```

## 🎯 Routes

3. **Configure environment variables**

```bash- `/` - Redirects to dashboard

cp .env.example .env- `/login` - Authentication (Week 4)

```- `/dashboard` - Microsite list (Week 4)

- `/editor/:id` - **Drag & drop editor** ⭐

Edit `.env` and set:

```env## 🧪 How to Use

VITE_API_URL=http://localhost:3000

VITE_STRIPE_PUBLISHABLE_KEY=your_stripe_key1. Navigate to `/editor/new`

```2. Drag blocks from the left panel to the canvas

3. Click a block to select it

4. **Start development server**4. Edit properties in the right panel

```bash5. See changes in real-time on the canvas

npm run dev6. Reorder blocks using the grip handle (≡)

```7. Delete blocks with the trash icon



The app will be available at `http://localhost:5173`## 📋 Week 1 Roadmap



## 🏗️ Build for Production- [x] Setup Vite + React + TypeScript

- [x] Configure TailwindCSS v4

```bash- [x] Install Shadcn UI

# Build optimized production bundle- [x] Add Lucide Icons + Framer Motion

npm run build- [x] Setup React Router

- [x] Create project structure

# Preview production build locally- [x] Build three-panel editor layout

npm run preview- [x] Implement drag & drop (dnd-kit)

```- [x] Add block palette

- [x] Create canvas with live preview

## 📁 Project Structure- [x] Build block inspector

- [x] Add real-time editing

```- [x] Support image upload + URL

src/

├── components/          # React components## 🔜 Next Steps (Week 2)

│   ├── blocks/         # Content blocks (Profile, Hero, etc.)

│   ├── editor/         # Editor UI (Canvas, Inspector, etc.)- [ ] Install Tiptap rich text editor

│   ├── ui/             # Reusable UI components (shadcn/ui)- [ ] Add text formatting (bold, italic, links)

│   ├── settings/       # Settings pages- [ ] Block styling options (colors, alignment)

│   └── accessibility/  # A11y components- [ ] Font selection

├── pages/              # Route pages- [ ] Color pickers

├── lib/                # Utilities and helpers- [ ] Button style presets

│   └── api/           # API client modules- [ ] Image crop/fit options

├── contexts/           # React contexts (Theme, Payment)- [ ] Block templates

├── hooks/              # Custom React hooks

├── data/               # Static data (templates, presets)## 🐛 Known Issues

├── types/              # TypeScript type definitions

└── styles/             # Global styles- Buttons are intentionally non-clickable in editor (will work on published microsites)

```- Images use base64 encoding (will switch to S3/Cloudinary in Week 3)

- No data persistence yet (coming in Week 3)

## 🎨 Key Components

## 📝 Development Notes

### Editor Layout

The main editing interface with three panels:### TailwindCSS v4 Setup

- **Blocks Panel**: Drag blocks to add contentThis project uses TailwindCSS v4 which requires:

- **Canvas**: Live preview with device frames- \`@tailwindcss/postcss\` plugin

- **Inspector Panel**: Customize selected blocks- \`@import "tailwindcss"\` instead of \`@tailwind\` directives



### Block System### Path Aliases

Each block type has:Use \`@/\` to import from \`src/\`:

- **Block Component**: Renders the block on canvas```typescript

- **Inspector**: Edit block propertiesimport { Block } from '@/types';

- **Default Content**: Initial values for new blocksimport { cn } from '@/lib/utils';

```

### Theme System

Centralized theming with:## 🤝 Contributing

- **PageTheme**: Color schemes, fonts, backgrounds

- **Theme Gallery**: Pre-made professional themesThis is a learning project following a 10-week development plan. Each week builds upon the previous week's foundation.

- **Live Preview**: See changes in real-time

## 📄 License

## 🔌 API Integration

MIT

All API calls are centralized in `src/lib/api/`:

---

```typescript

import { micrositeApi } from '@/lib/api';**Current Status**: Week 1 Complete ✅  

**Next Milestone**: Week 2 - Rich Text & Styling

// Create microsite
const microsite = await micrositeApi.create({
  title: 'My Site',
  layout: blocks,
  theme: pageTheme
});

// Update microsite
await micrositeApi.update(id, { title: 'New Title' });

// Publish
await micrositeApi.publish(id);
```

## 🎯 Available Scripts

```bash
npm run dev          # Start dev server
npm run build        # Build for production
npm run preview      # Preview production build
npm run lint         # Run ESLint
npm run type-check   # TypeScript type checking
```

## 🌈 Theme Customization

Themes can be customized via the Theme Gallery or Design Panel:

```typescript
const myTheme: PageTheme = {
  id: 'custom',
  name: 'My Theme',
  colors: {
    primary: '#6366f1',
    secondary: '#8b5cf6',
    accent: '#ec4899',
    background: '#ffffff',
    text: '#1f2937'
  },
  fonts: {
    heading: 'Inter',
    body: 'Inter'
  },
  borderRadius: 'rounded-xl',
  // ... more options
};
```

## 📱 Responsive Breakpoints

- **Mobile**: < 768px
- **Tablet**: 768px - 1024px
- **Desktop**: > 1024px

All blocks are designed mobile-first and adapt to larger screens.

## ♿ Accessibility

- WCAG 2.1 Level AA compliant
- Keyboard navigation support
- Screen reader friendly
- Focus management
- Skip links
- ARIA labels

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License.

## 🙏 Acknowledgments

- [shadcn/ui](https://ui.shadcn.com/) - Beautiful UI components
- [Tailwind CSS](https://tailwindcss.com/) - Utility-first CSS
- [DnD Kit](https://dndkit.com/) - Drag and drop toolkit
- [Tiptap](https://tiptap.dev/) - Rich text editor

## 📞 Support

For issues and questions:
- Create an issue on GitHub
- Check existing documentation
- Review the [backend repository](https://github.com/Scanly-io/qr-backend)

---

Built with ❤️ using React, TypeScript, and Vite
