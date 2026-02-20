# SignalTrace — Vercel Deployment Guide

## What's in this folder

```
signtrace-vercel/
├── api/
│   └── analyze.js       ← Serverless function (holds your API key securely)
├── public/
│   └── index.html       ← The full SignalTrace app
├── vercel.json          ← Vercel routing config
└── README.md            ← This file
```

---

## Deploy in 5 steps

### Step 1 — Create a free Vercel account
Go to https://vercel.com and sign up (free). Connect your GitHub account when prompted.

### Step 2 — Upload this project
You have two options:

**Option A — Drag & Drop (easiest)**
1. Go to https://vercel.com/new
2. Click "Browse" or drag the entire `signtrace-vercel` folder onto the page
3. Vercel will auto-detect the project

**Option B — Via GitHub**
1. Create a new repo on GitHub and push this folder
2. In Vercel, click "Add New Project" → import from GitHub
3. Select your repo

### Step 3 — Add your Anthropic API key
1. In Vercel, go to your project → **Settings** → **Environment Variables**
2. Click **Add New**
3. Name: `ANTHROPIC_API_KEY`
4. Value: your Anthropic API key (starts with `sk-ant-...`)
5. Make sure **Production**, **Preview**, and **Development** are all checked
6. Click **Save**

Get your API key at: https://console.anthropic.com/settings/keys

### Step 4 — Deploy
Click **Deploy**. Vercel will build and deploy in about 30 seconds.

### Step 5 — Open your live URL
Vercel gives you a URL like `https://signtrace-abc123.vercel.app`
That's your live app — share it with anyone.

---

## Updating the app
Any time you want to make changes:
- If using GitHub: push a commit and Vercel auto-deploys
- If using drag & drop: re-drag the updated folder to Vercel

---

## Pricing
- Vercel free tier: plenty for early usage (100GB bandwidth/month)
- Anthropic API: ~$0.003 per analysis (very cheap)
- You only pay if you scale up

---

## Custom domain (optional)
In Vercel → Settings → Domains → add your own domain (e.g. `signtrace.io`)
