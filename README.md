# Football Lineup Website

This is a static HTML site organised around a football lineup. The main page links to separate goalkeeper, defender, midfielder and forward pages, with local player images.

## Project goal

Let visitors explore a football lineup through linked position pages and player images.

![Project goal: football-lineup-web](docs/goals/project-focus-v1.png)

AI-generated concept illustration. Device appearance, interface layout and example graphics are illustrative, not project photographs or measured results.

## Where it could be used

The same page structure could be adapted into a small club or school-team showcase: introduce the lineup, group players by position and link to individual information. It is suitable for content that can be maintained as static pages. Live scores, automatic roster updates and user accounts would be separate additions.

## At a glance

![Football website navigation](docs/flowcharts/football.png)

Overview reconstructed from the documented project and code. Results and verification limits are described below. [SVG](docs/flowcharts/football.svg)

## What is in the site

The site is organised as a set of static pages. The main page introduces the lineup, and links take the reader to the position pages. The pages combine HTML structure with locally referenced player images. There is no Python application behind the site; the optional server below only serves the files to a browser.

This was an exercise in connecting pages and assets, rather than a data-driven lineup generator. The football content gives the navigation a concrete subject. It was created by Sangheon Park as an early web-development exercise.

## Viewing the project

Open [main.html](main.html) in a browser, or serve the repository locally:

```sh
python -m http.server 8000 --bind 127.0.0.1
```

Then open `http://127.0.0.1:8000/main.html`.

The position pages are [gk.html](gk.html), [df.html](df.html), [mf.html](mf.html) and [fw.html](fw.html). Player images and other third-party assets retain their original ownership.

To understand the implementation, begin with `main.html`, follow one position link and inspect the image references in that page. Keep the original folder layout when opening or serving the site; relative links depend on where the pages and images sit. Editing one HTML file is enough to experiment with that page without introducing a build tool or backend.

The local-server command is a viewing option, not a deployment step. It does not turn the project into a hosted service or add live football data.

The files and their paths have been inspected. A cross-browser or accessibility review has not been completed, and this repository is not deployed through GitHub Pages.

[Original repository](https://github.com/sangheon47/fifaweb). Original history and attribution are retained.
