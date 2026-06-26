# Helvetia Bau & Renovation Deployment

Production URL:

```text
https://picartweb.com/bau/
```

Upload the full website folder contents into the server subfolder:

```text
public_html/bau/
```

The `.htaccess` file must be uploaded into the same `/bau/` folder as `index.html`.

## Clean URLs

The production routes are:

```text
/bau/              -> index.html
/bau/leistungen    -> services.html
/bau/projekte      -> projects.html
/bau/ueber-uns     -> about.html
/bau/kontakt       -> contact.html
/bau/impressum     -> impressum.html
/bau/datenschutz   -> datenschutz.html
/bau/404.html      -> custom 404 page
```

Old `.html` URLs redirect permanently to the clean URLs, for example:

```text
/bau/services.html -> /bau/leistungen
/bau/contact.html  -> /bau/kontakt
```

## Server Features

The `.htaccess` file includes:

- HTTPS redirect
- Directory listing disabled
- Clean URL rewrites for the `/bau/` subfolder
- Redirects from old `.html` URLs
- Custom 404 page at `/bau/404.html`
- Long browser caching for CSS, JavaScript, images, and fonts
- No-cache headers for HTML files
- Gzip/deflate compression
- Security headers:
  - `X-Content-Type-Options`
  - `X-Frame-Options`
  - `Referrer-Policy`
  - `Permissions-Policy`

## Compatibility Notes

Internal links use `/bau/...` clean paths, while assets remain relative:

```text
assets/css/style.css
assets/js/script.js
assets/images/...
```

This keeps CSS, JavaScript, images, the language switcher, cookie banner, and Google Maps iframe working from the `/bau/` subfolder.

## Post-Upload Checklist

After uploading, test:

- `https://picartweb.com/bau/`
- `https://picartweb.com/bau/leistungen`
- `https://picartweb.com/bau/projekte`
- `https://picartweb.com/bau/ueber-uns`
- `https://picartweb.com/bau/kontakt`
- `https://picartweb.com/bau/impressum`
- `https://picartweb.com/bau/datenschutz`
- `https://picartweb.com/bau/services.html` redirects to `/bau/leistungen`
- `https://picartweb.com/bau/contact.html` redirects to `/bau/kontakt`
- A missing page shows `/bau/404.html`

If clean URLs return 404, confirm Apache `mod_rewrite` and `.htaccess` overrides are enabled for the `/bau/` directory.
