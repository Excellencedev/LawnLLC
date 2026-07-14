# The Lawn Butler LLC — Lawn Care Website

A high-converting single-page website for **The Lawn Butler LLC**, a lawn care company in Dallas, TX.

## What's included

- `index.html` — Single-page site with hero/contact form, services, reviews, why us, FAQ, and final CTA.
- `.github/workflows/deploy.yml` — GitHub Actions CI workflow that deploys to GitHub Pages.

## Local preview

No build step is required. Open `index.html` directly in your browser, or run a simple local server:

```bash
python -m http.server 8000
```

Then visit `http://localhost:8000`.

## Deploy to GitHub Pages

1. Create a new GitHub repository.
2. Push these files to the `main` (or `master`) branch.
3. Go to **Settings → Pages** in your repo.
4. Under **Source**, select **GitHub Actions**.
5. The workflow in `.github/workflows/deploy.yml` will run automatically and publish the site.

Your site will be live at `https://<your-username>.github.io/<repository-name>/`.

## Form setup

The contact form is configured for [Formspree](https://formspree.io):

1. Create a free Formspree form.
2. Replace `YOUR_FORM_ID` in the form `action` inside `index.html`:

```html
<form id="quote-form" action="https://formspree.io/f/YOUR_ACTUAL_FORM_ID" method="POST">
```

3. After a visitor submits the form, you'll receive an email with their details.

If you prefer a different form backend, replace the `<form>` action and update the submission handler in the `<script>` at the bottom of `index.html`.

## Customization

- Business info (name, address, phone, hours): edit the header, hero, and footer sections of `index.html`.
- Reviews: update the `#reviews` section with current customer testimonials.
- Services: edit the `#services` grid.
- Brand colors: adjust the `brand` color palette in the Tailwind config block inside `index.html`.

## License

Provided as-is for The Lawn Butler LLC website project.
