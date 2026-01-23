# Talli - Group Project Management

AI-powered group project management for students.

## 🚀 Deployment Instructions

### Step 1: Push to GitHub

1. Create a new GitHub repository called `talli-app`
2. Upload all these files to the repository:
   - `index.html`
   - `api/generate.js`
   - `vercel.json`
   - `package.json`
   - `logo.png` (add your logo)
   - `manifest.json` (if you have one)

### Step 2: Deploy to Vercel

1. Go to [vercel.com](https://vercel.com) and sign up/login with GitHub
2. Click "Add New Project"
3. Import your `talli-app` repository
4. **IMPORTANT:** Add your environment variable:
   - Click "Environment Variables"
   - Name: `OPENROUTER_API_KEY`
   - Value: `your-openrouter-api-key-here`
5. Click "Deploy"

### Step 3: Connect Your Domain

1. In Vercel dashboard, go to your project
2. Click "Settings" → "Domains"
3. Add `talli-app.com`
4. Vercel will show you DNS records to add

### Step 4: Update DNS at Your Domain Registrar

At your domain registrar (where you bought talli-app.com), add these DNS records:

**Option A: Using Vercel DNS (Recommended)**
- Type: `A`
- Name: `@`
- Value: `76.76.21.21`

- Type: `CNAME`
- Name: `www`
- Value: `cname.vercel-dns.com`

**Option B: Using nameservers**
Change nameservers to:
- `ns1.vercel-dns.com`
- `ns2.vercel-dns.com`

### Step 5: Wait for DNS propagation

This can take 10 minutes to 48 hours. You can check status at:
https://dnschecker.org/#A/talli-app.com

---

## 🔒 Security Notes

- Your OpenRouter API key is stored securely in Vercel's environment variables
- It's NEVER exposed to the browser/client
- All API calls go through the serverless function (`/api/generate`)

## 📁 File Structure

```
talli-app/
├── index.html          # Main app
├── api/
│   └── generate.js     # Secure API proxy (hides your key)
├── vercel.json         # Vercel configuration
├── package.json        # Project config
├── logo.png            # Your logo
└── manifest.json       # PWA manifest (optional)
```

## 🎉 You're Done!

Your app will be live at:
- https://talli-app.com
- https://www.talli-app.com
