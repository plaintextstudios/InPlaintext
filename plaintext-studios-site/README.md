# Plaintext Studios website

A static GitHub Pages site for Plaintext Studios: articles, podcasts, and blogging.

## Files

- `index.html` — homepage content
- `styles.css` — visual design inspired by the logo: pastel cream, coral, gold, geometric forms
- `script.js` — tiny helper for the footer year
- `CNAME.example` — rename to `CNAME` and replace with your real domain when ready

## Publish on GitHub Pages

1. Create a new GitHub repository, for example `plaintext-studios`.
2. Upload these files to the repository root.
3. Go to **Settings → Pages**.
4. Under **Build and deployment**, choose:
   - Source: `Deploy from a branch`
   - Branch: `main`
   - Folder: `/root`
5. Save.
6. Your temporary site will be at `https://YOUR-GITHUB-USERNAME.github.io/plaintext-studios/`.

## Connect a GoDaddy domain

In GitHub:
1. Go to **Settings → Pages → Custom domain**.
2. Enter your domain, for example `plaintextstudios.com`.
3. Save.
4. GitHub will create or expect a `CNAME` file in your repository.
5. After DNS works, enable **Enforce HTTPS**.

In GoDaddy DNS, add these records:

### For the root/apex domain, like `plaintextstudios.com`

Add four A records:

| Type | Name | Value |
| --- | --- | --- |
| A | @ | 185.199.108.153 |
| A | @ | 185.199.109.153 |
| A | @ | 185.199.110.153 |
| A | @ | 185.199.111.153 |

Optional but recommended: add GitHub Pages AAAA records too, from the current GitHub Docs page.

### For `www.plaintextstudios.com`

Add a CNAME record:

| Type | Name | Value |
| --- | --- | --- |
| CNAME | www | YOUR-GITHUB-USERNAME.github.io |

Then in GitHub Pages, use either the apex domain or `www` as your custom domain. DNS can take a few minutes to 48 hours to propagate.
