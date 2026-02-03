# nolit.ai Website

Landing page for nolit.ai — the privacy-first macOS meeting copilot.

## Deployment

This site is deployed via GitHub Pages.

### Setup Instructions

1. Create a new GitHub repository (private): `your-username/nolitai-website`

2. Push this code:
   ```bash
   cd nolitai-website
   git init
   git add .
   git commit -m "Initial website"
   git branch -M main
   git remote add origin git@github.com:your-username/nolitai-website.git
   git push -u origin main
   ```

3. In GitHub repository settings:
   - Go to Settings → Pages
   - Source: Deploy from branch
   - Branch: main / (root)
   - Save

4. For custom domain (nolit.ai):
   - Add A records pointing to GitHub Pages IPs:
     - 185.199.108.153
     - 185.199.109.153
     - 185.199.110.153
     - 185.199.111.153
   - Or add CNAME record pointing to `your-username.github.io`
   - Enable "Enforce HTTPS" in GitHub Pages settings

## Local Development

Simply open `index.html` in a browser, or use a local server:

```bash
# Python 3
python -m http.server 8000

# Then open http://localhost:8000
```

## Structure

```
nolitai-website/
├── index.html      # Main landing page
├── CNAME           # Custom domain config
├── .nojekyll       # Disable Jekyll processing
└── README.md       # This file
```

## Waitlist

The waitlist form currently stores emails in localStorage. To collect emails properly:

1. **Option A**: Use a service like Formspree, Netlify Forms, or Buttondown
2. **Option B**: Add a simple backend (Cloudflare Workers, Vercel Functions)
3. **Option C**: Connect to your preferred email marketing tool

---

**nolit.ai** — Not Lost in Translation, lit up by AI.
