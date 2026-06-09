# Kipu Website

Static website for the iOS app **Kipu**. It is designed to be published on GitHub Pages with a simple landing page at `/`, the Privacy Policy at `/privacy/`, Terms and Conditions at `/terms/`, and support at `/support/`.

## Files

- `index.html` - Simple landing page, accessible from the site root.
- `privacy/index.html` - Main Privacy Policy page, accessible from `/privacy/`.
- `privacy.html` - Lightweight redirect to `privacy/index.html` for local compatibility.
- `terms/index.html` - Terms and Conditions page, accessible from `/terms/`.
- `terms.html` - Lightweight redirect to `terms/index.html` for local compatibility.
- `support/index.html` - Support page, accessible from `/support/`.
- `support.html` - Lightweight redirect to `support/index.html` for local compatibility.
- `styles.css` - Responsive, dependency-free styling.

## App Store Review Checklist

The Privacy Policy currently states that Kipu:

- Does not require an account.
- Does not operate an advertising network or analytics backend.
- Stores bookmark data and app settings locally on the user's device.
- Does not upload the bookmark library to a Kipu server.
- Uses network requests for link metadata, thumbnails, in-app browsing, sharing/import/export flows, and purchase management.
- Uses Apple App Store / StoreKit and RevenueCat for Kipu Pro purchases, subscriptions, entitlements, and restoration.
- May use device features such as local notifications, file picker, photo picker, secure storage/Keychain, and device authentication.

Before submitting to App Store Review, confirm that these statements match the shipping build and App Store Connect privacy answers. If the app uses any additional SDK, backend service, crash reporting, analytics, authentication, CloudKit, advertising, or user account system, update `privacy/index.html` and the App Store privacy label before submitting.

Use the public `/privacy/` URL as the Privacy Policy URL in App Store Connect.

The Terms page still includes placeholders for jurisdiction and optional website/address details. Replace those before publishing if they are required for your submission or jurisdiction.

## Preview Locally

Open `index.html` directly in a browser for the landing page, `privacy/index.html` for the Privacy Policy, `terms/index.html` for the Terms and Conditions, or `support/index.html` for support.

For the clean `/privacy/` route locally, serve the folder with a static server first:

```bash
python -m http.server 8000
```

Then open:

```text
http://localhost:8000/
http://localhost:8000/privacy/
http://localhost:8000/terms/
http://localhost:8000/support/
```

## Publish With GitHub Pages

1. Create a new GitHub repository, for example `Kipu-web`.
2. Commit and push these files to the repository's default branch:

   ```bash
   git init
   git add index.html privacy/index.html privacy.html terms/index.html terms.html support/index.html support.html styles.css README.md
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

9. Use the `/privacy/` URL in App Store Connect under the app's Privacy Policy URL field.
