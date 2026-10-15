# 0bsh3ll

My personal blog on malware analysis, reverse engineering, AI and certifications.

🌐 **Live site:** https://0bsh3ll.github.io

## Posts

| Category | Post |
|---|---|
| Certifications | [How I Passed GREM in a Month with Self-Study](https://0bsh3ll.github.io/certs/grem-self-study.html) |
| AI & Automation | [Loki — A Local AI Agent That Actually Does Things](https://0bsh3ll.github.io/ai/loki.html) |

## Structure

```
index.html          # homepage (built by Jekyll from _data/posts.yml)
_data/posts.yml     # list of posts shown on the homepage
_config.yml         # Jekyll config
ai/  certs/  cool/  lab/  re/  research/  scripts/
                    # one folder per category; each has a template.html
```

## Adding a post

1. Copy the `template.html` from the category folder, e.g. `cp re/template.html re/my-post.html`.
2. Write the post.
3. Add an entry to the top of `_data/posts.yml`:
   ```yaml
   - tag: re
     tag_label: "Reverse Engineering"
     date: "2026-10-15"
     title: "My Post"
     excerpt: "One-line summary."
     url: "re/my-post.html"
   ```
4. Commit and push. GitHub Pages rebuilds the site automatically.

## Run locally

With Docker:

```bash
sudo docker run --rm -v "$PWD":/srv/jekyll -v jekyll_gems:/usr/local/bundle -w /srv/jekyll -p 4000:4000 \
  jekyll/jekyll sh -c "bundle install && bundle exec jekyll serve --host 0.0.0.0 --force_polling"
```

Then open http://localhost:4000.

## Connect

[GitHub](https://github.com/0bsh3ll) · [LinkedIn](https://www.linkedin.com/in/0bsh3ll/)

---

All content is for educational and research purposes only.
