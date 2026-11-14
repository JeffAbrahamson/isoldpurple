# isoldpurple.com

A tiny static site built with [Hugo](https://gohugo.io/).

    hugo server     # preview at http://localhost:1313/
    hugo --minify   # build into public/

Content lives in `content/`, templates in `layouts/`, styles in `assets/css/`.
Pages are published at flat URLs (`/whois-begin.html`, …) via `uglyURLs`.

Deployed on Cloudflare: the build command is `hugo --gc --minify` and
`npx wrangler deploy` uploads `public/` as static assets, as configured in
`wrangler.jsonc`. The Worker name there must match the Cloudflare project name.
