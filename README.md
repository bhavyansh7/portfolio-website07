# Bhavyansh Rathore — Portfolio

This is a lightweight static site. It runs locally with Python and deploys directly to Vercel with no build step.

## Run locally

From this folder, run:

```sh
python3 -m http.server 4173
```

Then open <http://localhost:4173>.

## Add your videos

The five project frames are designed placeholders. To show a video, edit `index.html` and replace the `<div class="project-visual ...">…</div>` inside a project with a `<video>` element, for example:

```html
<video class="project-video" controls playsinline poster="media/project-1.jpg">
  <source src="media/project-1.mp4" type="video/mp4">
</video>
```

Place the video and optional poster image in a `media/` folder beside `index.html`. Add this rule to `styles.css`:

```css
.project-video { display: block; width: 100%; height: 100%; object-fit: cover; }
```

For portrait Reels and Shorts, `object-fit: cover` keeps the frame filled; use a 9:16 export and adjust `object-position` if needed. Update project titles, descriptions and durations in `index.html` at the same time.

## Deploy to Vercel

Import this folder as a Vercel project. Choose **Other** as the framework preset and leave the build command and output directory empty. Vercel serves `index.html` as a static site. `vercel.json` enables clean URLs.

