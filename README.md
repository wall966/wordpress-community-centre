🇬🇧 English | [🇫🇷 Français](README.fr.md)

# WordPress – Community Centre Website

Custom code I developed during my web developer internship (August–October 2026) for the website of a community centre in Amplepuis, France.

**Context:** WordPress · Pixfort theme · Elementor + WPBakery · OVH hosting (Apache)

🔗 **Live website:** [centresocialduparc.fr](https://www.centresocialduparc.fr)

## Preview

![Home page – hero banner](screenshots/accueil.png)

![“Nos Pôles d'activités” section](screenshots/poles-activites.png)

## What I did

- **Custom PHP snippets** using WordPress hooks (`wp_print_styles`, `the_content`):
  - remove unused WPBakery CSS on pages that don't need it
  - automatically display attached documents and a photo carousel on "sharing" posts, with secured output (`esc_url`, `esc_html`, `esc_attr`)
- **Performance:** PageSpeed Insights analysis, browser caching via `.htaccess`, page caching, WebP image compression
- **Security:** forced HTTPS redirect, HTTP security headers (HSTS, X-Frame-Options, COOP), database backups and a staging site
- **Online registration forms** (Ninja Forms): HTML email templates with automatic file attachments sent to the centre's office
- **Hosting and domain management (OVH):** MySQL databases, DNS configuration and subdomain redirects
- **Technical handbook** written to help other developers take over the site

## Repository structure

| Folder | Content |
| --- | --- |
| `snippets/` | Custom PHP snippets (added with WPCode) |
| `htaccess/` | Commented `.htaccess` example (cache, HTTPS, security headers) |
| `ninja-forms/` | HTML email templates for the registration forms |
| `docs/` | Notes on performance analysis and lessons learned |
| `screenshots/` | Website screenshots |

## Stack

WordPress · PHP · CSS · HTML · Apache (`.htaccess`) · MySQL · OVH

## What I learned

- How WordPress hooks work, and why the **timing** of a hook matters (a CSS removed too early was added back by the theme)
- Testing one change at a time and always clearing the cache before checking the result
- Not every PageSpeed warning should be fixed: some "optimisations" broke the layout, so I learned to measure and roll back



