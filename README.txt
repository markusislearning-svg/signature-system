# Online iPhone Signature System

This version uses:
- GitHub Pages for free web hosting
- Supabase Free for centralized storage
- Touch / Apple Pencil signature capture
- Name + Department + Signature
- Clear / Reset Signature
- Mobile-friendly iPhone/iPad interface

## Part 1 — Create the free Supabase database

1. Go to https://supabase.com/
2. Create a free account.
3. Create a new project.
4. Open SQL Editor.
5. Paste the contents of `supabase_setup.sql`.
6. Run it.
7. Open Project Settings -> Data API/API.
8. Copy the Project URL and the public/publishable (anon) key.

## Part 2 — Connect the website

Open `config.js`.

Replace:
PASTE_YOUR_SUPABASE_PROJECT_URL_HERE
PASTE_YOUR_SUPABASE_ANON_OR_PUBLISHABLE_KEY_HERE

Do NOT put a Supabase service-role/secret key in this file.

## Part 3 — Put it online with GitHub Pages

1. Create/sign into a free GitHub account.
2. Create a NEW PUBLIC repository, for example:
   signature-system
3. Upload these 3 files:
   - index.html
   - config.js
   - supabase_setup.sql
4. Open the repository's Settings.
5. Select Pages.
6. Under Build and deployment, choose:
   - Source: Deploy from a branch
   - Branch: main
   - Folder: / (root)
7. Save.
8. GitHub will give you a website address similar to:
   https://YOUR-USERNAME.github.io/signature-system/

## Part 4 — Use it on iPhone

1. Open the GitHub Pages address in Safari.
2. Test Name, Department and Signature.
3. Tap Share.
4. Tap Add to Home Screen.
5. Open the new Signature System icon like an app.

## Important security note

The website uses only the public/publishable Supabase key. That key is intended for browser applications. Database Row Level Security is enabled so anonymous users can INSERT submissions but cannot SELECT submitted signatures.

For an organization-wide system, an administrator dashboard with login can be added later.
