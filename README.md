# bridged.com

Production source for https://bridged.com, the Bridged landing site.

Static HTML and CSS, no build step. Hosted on Netlify (project `bridged-com`,
team Bridged LLC). Every push to `main` deploys automatically.

## Pages

| Path | Purpose |
| --- | --- |
| `index.html` | Home: hero, mission, blueprint cards, contact form |
| `case-study.html` | Case study: MEDam.com, Armenia |
| `thanks.html` | Shown after a contact-form submission |
| `404.html` | Not-found page (Netlify serves it automatically) |
| `assets/styles.css` | All styling; design tokens from the Bridged design system |
| `assets/` | Logo files, favicon, Open Graph image |
| `robots.txt`, `sitemap.xml` | Search engine files |
| `netlify.toml` | Netlify settings (publish root, security headers) |

## How updates work

1. Design changes are made in the Claude Design canvas ("bridged.com" boards).
2. Claude carries the change into these files and pushes a commit to `main`.
3. Netlify builds and publishes within about a minute. Every deploy is kept,
   so any earlier version can be restored from Netlify > Deploys > Publish deploy.

## Contact form

The form in `index.html` uses Netlify Forms (`data-netlify="true"`, form name
`contact`, honeypot `bot-field`). Submissions are stored under Netlify > Forms
and emailed to vrej@bridged.com. If the form's fields change, Netlify picks up
the new definition on the next deploy.

## Copy rules

MEDam.com copy follows the MEDam.com Approved Copy sheet: always "MEDam.com",
tagline "Armenia's Official Medical Tourism Partner.", only the approved MOU
sentence for the government relationship, figures dated "as of [month year]",
no em dashes, emoji or exclamation marks.
