# animeshja.in

Animesh Jain’s personal website. Static HTML and CSS; no build process or backend required.

## Source

- `dist/index.html`: page content
- `dist/style.css`: responsive styling
- `dist/icon.svg`: logo/favicon
- `.github/workflows/pages.yml`: GitHub Pages publication on pushes to main

For local viewing: `python -m http.server 8000 --directory dist`.

## Independent hosting on GitHub Pages

1. Store this source in `animeshj9/animeshja.in`.
2. In repository Settings → Pages, select GitHub Actions as the source.
3. Run the Publish website workflow (later pushes to main run it automatically).
4. Set the custom domain to `animeshja.in` in Settings → Pages, before editing DNS.
5. In Squarespace DNS, replace website A records for `@` with these GitHub Pages addresses:
   - 185.199.108.153
   - 185.199.109.153
   - 185.199.110.153
   - 185.199.111.153
6. For `www`, set CNAME to `animeshj9.github.io` and check GitHub's custom-domain setup for the desired redirect.
7. Preserve email DNS records. Once domain validation and the certificate finish, enable Enforce HTTPS.

Do not use the prior ChatGPT Sites A-record targets for this GitHub Pages setup. Squarespace remains the domain/DNS provider; GitHub serves the actual website. The browser URL remains animeshja.in.

GitHub Free supports Pages from public repositories. Pages from a private personal repository requires GitHub Pro. The `.openai` manifest belongs to the earlier Sites preview and is not needed by GitHub Pages; only `dist` is published.

Official documentation:
- https://docs.github.com/en/pages/getting-started-with-github-pages/using-custom-workflows-with-github-pages
- https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site
