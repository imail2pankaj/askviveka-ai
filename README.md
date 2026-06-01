# 🌌 AskViveka — Ancient Wisdom for Modern Life

AskViveka is a meditative, secular spiritual platform designed to help you navigate modern life's challenges—such as anxiety, fear, success, failure, and duty—using the timeless, authentic teachings of the **Bhagavad Gita**. 

By combining the depth of original scriptures and centuries-old commentary with state-of-the-art vector similarity AI, AskViveka guides you back to mental resilience, detached execution, and inner stillness.

---

## 🌟 Key Features

### 1. Context-Grounded AI Guidance
* **Ask Life's Questions**: State what is on your mind today, and receive warm, highly compassionate guidance that feels like a spiritual mentor.
* **Vector-Grounded Retrieval**: Powered by Postgres `pgvector` similarity search, the AI retrieves relevant verses and authoritative commentaries to formulate authentic, context-rich responses rather than generalized models.

### 2. Meditative Premium Design System
* **Aesthetic Visual Excellence**: Designed with a stunning, premium dark theme using custom glassmorphic panels, glowing radial backdrops, golden-gilded ornaments, and subtle twinkling animations.
* **Typographical Legibility**: Fully integrated with standard Tailwind CSS v4 dark mode to activate high-contrast text and responsive layouts designed specifically for spiritual reflection.

### 3. Unified User Journey & Protected Workflows
* **Exploratory Guest Access**: Anyone can search keywords, browse through chapters, view detailed commentaries, and draft prompts in the search boxes.
* **Seamless Authentication Loop**: Submitting a query redirects unauthenticated guests to sign up or log in. Once authenticated, they are automatically returned to `/ask` with their original prompt seamlessly processed and answered.
* **Saved Wisdom Portfolio**: Logged-in users can bookmark specific verses and maintain a persistent, interactive history of their previous AI reflections in a quiet sanctuary sidebar.

### 4. Administrator Console
* **Real-time Analytics**: A protected dashboard at `/admin` displaying real-time metrics for scriptures, chapters, verses, and commentators.
* **System Operations Logs**: Live logs tracking AI token usage, request statuses, endpoints, and popular user search terms to guide platform curation safely.

---

## 🛠️ Technology Stack

* **Framework**: [Next.js 16 (App Router)](https://nextjs.org/) utilizing React Server Components (RSC) and Server Actions for optimal performance and secure server-to-client operations.
* **Styling**: [Tailwind CSS v4](https://tailwindcss.com/) & `tw-animate-css` for animations, hover transitions, and glassmorphism.
* **Database & Auth**: [Supabase](https://supabase.com/) & PostgreSQL using `pgvector` for similarity calculations, and Supabase SSR for secure auth session persistence using cookies.
* **AI Engine**: [OpenAI API](https://openai.com/) — `gpt-4o` for compiling structured wisdom prompts and `text-embedding-3-small` for semantic vector embeddings.
* **Icons**: [Lucide React](https://lucide.dev/) for crisp, scalable meditative icons.

---

## 🚀 Getting Started

### 1. Requirements & Prerequisites
Ensure you have the following installed on your local machine:
* **Node.js**: `v18.x` or higher
* **Supabase CLI**: For local database seeding or a Supabase Cloud account.

### 2. Environment Setup
Create a `.env` file in the root directory of your project and populate it with your credentials:

```env
# Supabase Configuration
SUPABASE_URL=https://your-project-id.supabase.co
SUPABASE_ANON_KEY=your-supabase-anonymous-key
SUPABASE_SERVICE_ROLE_KEY=your-supabase-service-role-key

# OpenAI API Configuration
OPENAI_API_KEY=your-openai-api-key
```

### 3. Database Schema Migration
Initialize your database by running the SQL migration script located in the repository:
1. Go to your Supabase SQL Editor.
2. Open and copy the contents of `supabase_schema.sql`.
3. Execute the script to create user tables, scriptures, chapters, verses, commentators, conversations, bookmarks, and the `match_verses` pgvector vector cosine similarity function.

### 4. Installation & Local Development
Install dependencies and launch the hot-reloading development server:

```bash
# Install packages
npm install

# Start the dev server
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) with your browser to experience the meditative portal.

### 5. Production Optimization
Build the optimized bundle and test compilation:

```bash
# Build the Next.js application
npm run build

# Start the production server
npm run start
```

---

## 📂 Codebase Directory Tour

```text
├── app/
│   ├── admin/             # Admin console logs, analytics, and access gating
│   ├── api/ask/           # AI endpoint executing pgvector searches and LLM formulation
│   ├── ask/               # Client-side AI conversation panel and query routing
│   ├── auth/              # Email signup, credentials login, and OAuth callbacks
│   ├── bookmarks/         # Saved verses and personal sanctuaries
│   ├── chapters/          # Chapters, verse index lists, and commentator details
│   ├── search/            # Keyword and scripture term searches
│   ├── globals.css        # Core custom animations, gradients, and gilded border designs
│   └── layout.tsx         # Unified dark-mode shell, headers, and footer setups
├── components/            # Reusable components (Navbar, Footer, VerseCard, AskChatInterface)
├── lib/                   # Database clients, OpenAI helpers, utility classes, and custom types
└── supabase_schema.sql    # Complete PostgreSQL structure & pgvector math logic
```

---

## 🧘 Cosmic Meditations & Rules
AskViveka is designed with strict boundaries to ensure mental safety:
* **Detached Action**: Focus strictly on the process, duty, and spiritual equanimity (*Samatvam*), translating ancient truths into real-world modern resilience.
* **Secular Safety**: No temple-style or dogma overload. Focuses wholly on calming anxious minds through clean typography and highly accessible reflections.
* **No Therapeutic Gaps**: Explicitly states it does not replace professional clinical or medical advice.
