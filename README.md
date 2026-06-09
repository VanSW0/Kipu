# Kipu Privacy Policy

Static privacy policy site for the iOS app **Kipu**. It is designed to be published on GitHub Pages and used as the Privacy Policy URL in App Store Connect.

## Files

- `index.html` - Main Privacy Policy page, accessible from the site root.
- `privacy.html` - Lightweight redirect to the root policy page.
- `styles.css` - Responsive, dependency-free styling.

## Before Publishing

Replace every placeholder in `index.html`:

- `[APP STORE PRIVACY DETAILS: ...]`
- `[THIRD-PARTY SERVICE NAME AND PURPOSE, IF APPLICABLE]`
- `[LINK TO THIRD-PARTY PRIVACY POLICY, IF APPLICABLE]`
- `[OPTIONAL BUSINESS ADDRESS OR REGION]`
- Canonical URL in the `<link rel="canonical">` tag

Confirm these privacy details before submitting the URL to App Store Connect:

- Whether Kipu collects personal data directly.
- Whether Kipu uses analytics, crash reporting, advertising, payments, authentication, backend hosting, cloud storage, or other SDKs/services.
- Whether any collected data is linked to the user.
- Whether any collected data is used for tracking under Apple's App Privacy rules.
- How long data is retained and how users can request deletion.
- Whether the app is intended for children or has child-directed features.

This draft is not legal advice. Review it against Kipu's actual behavior and applicable laws before publishing.

## Preview Locally

Open `index.html` directly in a browser. No build step or local server is required.

## Publish With GitHub Pages

1. Create a new GitHub repository, for example `Kipu-web`.
2. Commit and push these files to the repository's default branch:

   ```bash
   git init
   git add index.html privacy.html styles.css README.md
   git commit -m "Add Kipu privacy policy site"
   git branch -M main
   git remote add origin https://github.com/YOUR-GITHUB-USERNAME/Kipu-web.git
   git push -u origin main
   ```

3. In GitHub, open the repository settings.
4. Go to **Pages**.
5. Under **Build and deployment**, set **Source** to **Deploy from a branch**.
6. Select the `main` branch and the `/root` folder, then save.
7. Wait for GitHub Pages to publish the site.
8. Your public HTTPS URL should look like:

   ```text
   https://YOUR-GITHUB-USERNAME.github.io/Kipu-web/
   ```

9. Update the canonical URL in `index.html` to the final GitHub Pages URL.
10. Use the final URL in App Store Connect under the app's Privacy Policy URL field.
