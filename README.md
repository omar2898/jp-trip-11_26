# Japan trip app (private)

The app is stored encrypted (`site.enc`). GitHub Actions decrypts it, locks it behind your password with StatiCrypt, and publishes it to GitHub Pages. Nothing readable is ever committed.

## Change the password

1. Repo **Settings → Secrets and variables → Actions**.
2. Edit **SITE_PASSWORD** and type the new password.
3. **Actions → Build and deploy → Run workflow**.

About a minute later the site uses the new password. Phones that ticked "Remember me" will ask for it once more.

## Secrets this repo needs

- `SITE_PASSWORD`: the password you type to open the app.
- `SOURCE_KEY`: decrypts `site.enc`. Don't change it.
