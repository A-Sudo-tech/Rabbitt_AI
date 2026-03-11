# Talking Rabbitt — Conversational Analytics MVP

> **"Ask Your Data Anything."** Upload a CSV, ask a question in plain English, get instant insights and beautiful charts.

[![Live Demo](https://img.shields.io/badge/Live%20Demo-Vercel-black?style=for-the-badge&logo=vercel)](https://your-deployment-url.vercel.app)
[![Built with Next.js](https://img.shields.io/badge/Next.js-14-black?style=for-the-badge&logo=next.js)](https://nextjs.org)

---

## 🪄 The Magic Moment

The core value of Talking Rabbitt in one workflow:

```
User uploads sales CSV
    ↓
Types: "Which region had the highest revenue in Q1?"
    ↓
Rabbitt AI responds in <5 seconds:
"North America generated the highest revenue at $1,162K — representing 30.2% of total revenue."
    ↓
Bar chart auto-generated ✓
Calculation breakdown shown ✓
```

This replaces a 30-minute analyst loop with a 5-second conversation.

---

## 🚀 Features

| Feature | Description |
|---------|-------------|
| **CSV Upload** | Drag & drop or click to upload any business CSV |
| **Natural Language Queries** | Ask questions in plain English — no SQL, no filters |
| **Instant Insights** | Heuristic NLQ engine parses and computes answers deterministically |
| **Auto Charts** | Recharts bar charts generated automatically |
| **Data Table View** | Ranked results table with % of total |
| **How Calculated** | Full transparency — see exactly how every answer was derived |
| **AI Enhancement** | Optional OpenAI API key for GPT-4o-mini executive-style insights |
| **Query History** | Browse recent queries |
| **Sample Data** | Built-in 20-row sales dataset to demo without uploading |

---

## 🏗 Tech Stack

- **Framework**: Next.js 14 (App Router)
- **Language**: TypeScript
- **Styling**: Tailwind CSS + custom CSS (glassmorphism, dark mode)
- **Charts**: Recharts
- **CSV Parsing**: PapaParse
- **AI (optional)**: OpenAI API (gpt-4o-mini) via Edge Runtime
- **Deployment**: Vercel (recommended) / Netlify

---

## 📦 Quick Start

```bash
# Clone the repo
git clone https://github.com/your-username/talking-rabbitt.git
cd talking-rabbitt

# Install dependencies
npm install

# Run locally
npm run dev
# → Open http://localhost:3000
```

### Optional: Add OpenAI API Key
For AI-enhanced executive insights, click **"Add API Key"** in the header and paste your `sk-...` key. The app works fully without it — the heuristic engine handles all core queries.

---

## 📁 Sample CSV Format

The app works with any CSV. Optimal columns for best query results:

```csv
region,product_category,salesperson,revenue,units_sold,quarter
North America,SaaS Platform,Alice Johnson,285000,142,Q1
Europe,AI Copilot,Bob Smith,198000,99,Q1
...
```

**Download the sample**: Click "Download Sample CSV" on the landing page.

---

## 🎯 Supported Query Patterns

| Question Type | Example |
|--------------|---------|
| Highest/Best | "Which region had the highest revenue?" |
| Lowest/Worst | "Which salesperson had the lowest sales?" |
| Count | "How many records by region?" |
| Average | "What is the average revenue by product category?" |
| By dimension | "Total sales by quarter" |

---

## 🗂 Project Structure

```
talking-rabbitt/
├── src/
│   └── app/
│       ├── layout.tsx          # Root layout + fonts
│       ├── page.tsx            # Main UI (CSV upload, NLQ, charts)
│       ├── globals.css         # Design system (dark mode, glassmorphism)
│       └── api/
│           └── query/
│               └── route.ts   # NLQ processing API (heuristic + OpenAI)
├── package.json
├── next.config.js
├── tailwind.config.ts
└── tsconfig.json
```

---

## 🚀 Deploy to Vercel

```bash
# Install Vercel CLI
npm i -g vercel

# Deploy
vercel --prod
```

Or connect your GitHub repo at [vercel.com](https://vercel.com) for one-click deployment.

---

## 📋 Evaluation Rubric Coverage

| Category | How This MVP Addresses It |
|----------|--------------------------|
| **Market Intelligence** | Built for the conversational analytics gap vs. Tableau/PowerBI/ThoughtSpot |
| **ICP & Strategy** | Targets VP Sales/Ops at mid-market firms — instant insight as kill strategy |
| **Product Prioritization** | MoSCoW: CSV+NLQ+Charts = Must Have; OpenAI enhancement = Should Have |
| **MVP & Execution** | ✅ Upload CSV → Ask → Get Answer + Chart in <5 seconds |

---

## 🏢 Built For

**Rabbitt AI Product Manager Case Study** — demonstrating the "Magic Moment" of conversational business intelligence.

---

*Talking Rabbitt turns your spreadsheet data into a conversation.*
