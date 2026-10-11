# Jiongze Yu — Personal Homepage

Live at <https://jiongze-yu.github.io/>. A single-page Jekyll site served by GitHub Pages (layout inspired by sainingxie.com).

## Editing

| What | Where |
|---|---|
| Name, email, links, avatar | `_config.yml` |
| About / Interests / News / Service / Education | `index.md` |
| Publications | `_data/publications.yml` (see the field list at the top) |
| Teaser videos and figures | `assets/teasers/` |
| Styles | `assets/css/main.css` |

Teaser clips are short (5–20 s), muted, 640 px wide H.264, e.g.

```bash
ffmpeg -ss 18 -t 12 -i input.mp4 -an -vf "scale=640:-2,fps=24" -c:v libx264 -crf 27 \
  -pix_fmt yuv420p -movflags +faststart assets/teasers/name.mp4
ffmpeg -i assets/teasers/name.mp4 -vframes 1 assets/teasers/name.jpg   # poster
```

## Local preview

```bash
bundle install && bundle exec jekyll serve
```
