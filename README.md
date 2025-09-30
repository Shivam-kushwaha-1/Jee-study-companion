# Jee-study-companion
# JEE Study Companion (React + Tailwind PWA)

This project is a **modern study planner and tracker** built for JEE aspirants, featuring timers, analytics, flashcards, and multiplayer leaderboard.

---

## 🚀 Features
- Smart Study Planner with adaptive goals
- Pomodoro + Stopwatch Timers
- Flashcards with spaced repetition
- Multiplayer Friends Leaderboard
- Analytics Dashboard with heatmap & reports
- Integrated Audio Player for focus music
- Progressive Web App (PWA) ready

---

## 📦 Installation
```bash
git clone https://github.com/your-username/jee-study-companion.git
cd jee-study-companion
npm install
npm run dev
```

---

## 🌐 Deployment
This project supports **automatic deployment** via **GitHub Actions + Vercel**.

### 🔹 GitHub Actions for Vercel
File: `.github/workflows/deploy-vercel.yml`
```yaml
name: Deploy to Vercel

on:
  push:
    branches:
      - main  # Deploys only when main branch updates

jobs:
  deploy:
    runs-on: ubuntu-latest

    steps:
      - name: Checkout repository
        uses: actions/checkout@v3

      - name: Install Node.js
        uses: actions/setup-node@v3
        with:
          node-version: 18

      - name: Install dependencies
        run: npm install

      - name: Build project
        run: npm run build

      - name: Deploy to Vercel
        uses: amondnet/vercel-action@v20
        with:
          vercel-token: ${{ secrets.VERCEL_TOKEN }}
          vercel-org-id: ${{ secrets.ORG_ID }}
          vercel-project-id: ${{ secrets.PROJECT_ID }}
          working-directory: ./
```

### 🔑 Setup
1. Go to [Vercel Dashboard](https://vercel.com/), create a project, and connect this GitHub repo.
2. Generate a **VERCEL_TOKEN** in Vercel.
3. Get **ORG_ID** and **PROJECT_ID** from your project settings.
4. Add them as GitHub repo secrets:
   - `VERCEL_TOKEN`
   - `ORG_ID`
   - `PROJECT_ID`

Now, every push to `main` will automatically deploy your app to Vercel 🚀

---

✅ You’re ready to auto-deploy your upgraded JEE Study Companion!
