# Connecting Your GoDaddy Domain to Your GitHub Pages Website

## 1. Purchase a Domain from GoDaddy

- Go to [GoDaddy Domains](https://www.godaddy.com/domains).
- Search for your desired domain (e.g., `yourresume.com`, `mbtechnologygroup.com`, etc.).
- Add the domain to your cart, complete the purchase, and set up your GoDaddy account.

## 2. Configure Your GitHub Pages Website

- Ensure your repository (e.g., `mbtechgru/christianmarrerobonilla.github.io`) contains your site's content (`index.html` for your resume).
- Find your GitHub Pages site URL (e.g., `https://mbtechgru.github.io/christianmarrerobonilla.github.io/`).
- Go to your repository's **Settings → Pages**.
- In the “Custom domain” field, enter your purchased domain name and save.

## 3. Update DNS Settings in GoDaddy

- Go to GoDaddy, log in, and navigate to your domain's **DNS Management**.
- For the root domain (e.g., `yourresume.com`):
  - Add or update four **A records** pointing to GitHub's IP addresses:
    ```
    185.199.108.153
    185.199.109.153
    185.199.110.153
    185.199.111.153
    ```
- For the `www` subdomain:
  - Add a **CNAME record**:
    ```
    Name: www
    Value: mbtechgru.github.io
    ```
- Remove any conflicting records for the same hostnames.

## 4. Finalize & Test

- DNS changes may take up to 24 hours to propagate.
- After DNS updates, visit your domain to confirm it’s working.
- In GitHub Pages settings, check “Enforce HTTPS” once it appears for security.

## 5. Troubleshooting

- GitHub creates a `CNAME` file in your repo—keep this file.
- If you see a GitHub 404 page, wait for DNS propagation and check your records.
- For help, see the official guide:  
  [GitHub Pages Custom Domain Docs](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site)

---

*You can copy this content and convert it to PDF, or let me know if you want further help converting/pushing as a file!*
