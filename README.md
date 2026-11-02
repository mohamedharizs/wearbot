# WEARBOT 👗👔

> Smart AI Outfit Recommendations & Digital Wardrobe Matching powered by Google Gemini.

Match your uploaded tops, bottoms, and accessories with AI-curated outfit recommendations, style coordination, and wardrobe organization.

---

## 🌟 Key Features

- **Digital Wardrobe**: Upload and organize your tops, bottoms, shoes, and accessories with image cropping, tagging, and camera capture.
- **AI Stylist (Gemini 2.5 / 2.0)**: Analyze your clothing items for color palette, style, formality, and seasonality to recommend combinations.
- **Interactive Outfit Shuffle**: Fast shuffle recommendations and custom generation modes (Casual, Formal, Streetwear, Date Night, etc.).
- **Camera & Image Editing**: Snap photos directly using your webcam/mobile camera or upload and crop wardrobe items.
- **Cloud Synchronization**: Optional Firebase Authentication and Firestore persistence for saving your wardrobe across devices.
- **Production-Ready**: Express full-stack API integration, Vercel Serverless Function rewrites, and Vite-optimized frontend.

---

## 🛠️ Tech Stack

- **Frontend**: [React 19](https://react.dev/), [TypeScript](https://www.typescriptlang.org/), [Vite](https://vitejs.dev/), [Tailwind CSS v4](https://tailwindcss.com/)
- **UI Components & Animation**: [Radix UI](https://www.radix-ui.com/), [Motion (Framer Motion)](https://motion.dev/), [Lucide React](https://lucide.dev/), [Sonner](https://sonner.emilkowal.ski/)
- **Backend / API**: [Express](https://expressjs.com/), [tsx](https://github.com/privatenumber/tsx)
- **AI Engine**: Google Gemini API via [`@google/genai`](https://www.npmjs.com/package/@google/genai)
- **Database & Auth**: [Firebase](https://firebase.google.com/) & Firestore

---

## 🚀 Getting Started

### Prerequisites

- [Node.js](https://nodejs.org/) (v18 or higher recommended)
- [npm](https://www.npmjs.com/) or [bun](https://bun.sh/)
- A Google Gemini API key (get one from [Google AI Studio](https://aistudio.google.com/))

### Installation

1. **Clone the repository**:
   ```bash
   git clone <repo-url>
   cd wearbot-main
   ```

2. **Install dependencies**:
   ```bash
   npm install
   ```

3. **Configure Environment Variables**:
   Copy the `.env.example` file to `.env`:
   ```bash
   cp .env.example .env
   ```
   Add your Gemini API key in `.env`:
   ```env
   GEMINI_API_KEY="your-gemini-api-key"
   ```

### Running Locally

Start the full-stack development server (Express API + Vite frontend):

```bash
npm run dev
```

Open your browser at `http://localhost:3000` (or the port specified in terminal).

---

## 📜 Available Scripts

| Command | Description |
|---|---|
| `npm run dev` | Runs the full-stack app with `tsx server.ts` |
| `npm run build` | Compiles the frontend with `vite build` |
| `npm run start` | Starts the production server using `server.ts` |
| `npm run preview` | Previews the production build locally |
| `npm run lint` | Runs TypeScript type checking (`tsc --noEmit`) |
| `npm run clean` | Cleans up the `dist/` directory and build artifacts |

---

## 📁 Project Structure

```text
├── api/                  # Vercel serverless function entry points
│   ├── index.ts
│   └── [...path].ts
├── public/               # Public assets, logos, and clothing presets
├── src/
│   ├── components/       # React UI components (Wardrobe, Camera, Upload, Dialogs)
│   │   └── ui/           # Shared primitive UI components (Radix/Tailwind)
│   ├── lib/              # AI limits, Firebase config, helpers, wardrobe storage
│   ├── App.tsx           # Main application view & state
│   ├── index.css         # Global styling and Tailwind directives
│   └── main.tsx          # React application entrypoint
├── server.ts             # Express server & Gemini API endpoints
├── vite.config.ts        # Vite configuration
└── package.json          # Project metadata & scripts
```

---

## 🔒 License

Private / MIT

