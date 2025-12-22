This repo now includes a simple static blog system.

How it works:
- `blog.html` is the front page that shows an excerpt (first 10 lines) from each post.
- Posts live in their own folder under `posts/<slug>/index.html`.
- Each post must include an element with class `post-content` (e.g., `<article class="post-content">...</article>`).
- The `posts/posts.json` file lists available posts and their `path`.

To add a new post:
1. Create `posts/my-new-post/index.html` with an `.post-content` element.
2. Add an entry to `posts/posts.json` with `title`, `slug`, and `path`.

Deploying to GitHub Pages:
- Push this repository to GitHub.
- In repository settings, enable GitHub Pages from the `gh-pages` branch or `main` (depending on your preference).
- To use a custom domain, add a `CNAME` file containing your domain (this repo already has one). Ensure your DNS points to GitHub Pages. For modern GitHub Pages, create these DNS records:
  - `A` records pointing to GitHub Pages IPs: `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153` (if using an apex domain).
  - Or create a `CNAME` record for `www` pointing to `yourusername.github.io` and use `www` as primary.

If you want, I can:
- Add more styling or pagination.
- Generate additional sample posts.
- Help set DNS records for your domain to point at GitHub Pages (tell me your domain and preferred apex/www choice).
