# ChronoClip

> Your personal knowledge base for YouTube content.

ChronoClip is a video bookmark manager that goes beyond simple playlists. It allows you to save YouTube videos, bookmark specific timestamps ("Clips"), add contextual notes, and organize your learning with tags. Perfect for researchers, students, and anyone who uses YouTube for education.

## Tech Stack

- **Framework:** Next.js (App Router)
- **Database:** Drizzle ORM (PostgreSQL/SQLite)
- **Styling:** Tailwind CSS & shadcn/ui
- **Video:** YouTube IFrame API

## Features

- **Precise Clipping:** Bookmark specific seconds in a video with one click.
- **Contextual Notes:** Add thoughts and summaries to every timestamp.
- **Tagging:** Organize clips by topic.
- **Instant Seek:** Click any saved clip to jump the player to that exact moment.
- **Library Management:** A clean dashboard for all your saved content.

## Getting Started

1. **Clone the repository**
   ```bash
   git clone <repo-url>
   cd chronoclip
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Setup Environment**
   Copy `.env.example` to `.env` and add your database credentials.
   ```bash
   cp .env.example .env
   ```

4. **Run Database Migrations**
   ```bash
   npx drizzle-kit push
   ```

5. **Start the development server**
   ```bash
   npm run dev
   ```

## Documentation

- [TASKLIST.md](./TASKLIST.md) - Project roadmap and status.
- [LEARNINGS.md](./LEARNINGS.md) - Technical insights and decisions.
- [.dev0/RULES.md](./.dev0/RULES.md) - AI coding guidelines.