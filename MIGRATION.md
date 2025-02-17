# Migrating MichelStorms.com from Wix to GitHub Pages

Your website, [michelstorms.com](https://www.michelstorms.com/), serves as a professional portfolio highlighting your expertise as a freelance Apple developer. The site includes sections such as a bio, testimonials, and a contact form for potential clients.

Transitioning from Wix to GitHub Pages is feasible, especially since your site primarily presents static content. Here's how you can approach the migration:

## 1. Content Backup
Manually extract your text, images, and media from Wix, as it doesn't offer a direct export feature.

## 2. Repository Setup
Create a new repository on GitHub named `michelstorms.github.io`. This naming convention enables GitHub Pages to serve your site at `https://michelstorms.github.io/`.

## 3. Site Reconstruction
Rebuild your site using static files. Given your technical background, you might consider using a static site generator like:
- [Jekyll](https://jekyllrb.com/) (GitHub Pages native support)
- [Hugo](https://gohugo.io/) (faster and more flexible)
- [Astro](https://astro.build/) (modern static site framework)

## 4. Contact Form Integration
Since GitHub Pages doesn't support server-side code, you'll need a third-party service to handle form submissions:
- [Formspree](https://formspree.io/)
- [Netlify Forms](https://www.netlify.com/products/forms/)

## 5. Custom Domain Configuration
To retain your existing domain, update the DNS settings to point to GitHub Pages. This involves modifying the `CNAME` and `A` records. GitHub's [documentation](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site) provides detailed guidance on this process.

## 6. Testing and Deployment
Before finalizing the switch:
- Test the site locally using a static server or Jekyll's built-in preview.
- Verify links, images, and responsiveness.
- Deploy and monitor for any issues.

---

By migrating to GitHub Pages, you'll gain:
✅ Greater control over design and functionality  
✅ Lower hosting costs  
✅ Faster performance  
