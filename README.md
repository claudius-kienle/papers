Website to host all pages for published papers with simple setup for new papers.

# Adding a new paper
You can serve the website (with hot reload) by executing
```bash
pixi run serve
```


1. **Authors and affiliations** are stored in `_data`. If your next paper includes a new author or affiliation, you have to add that to the corresponding .yml.
2. **Create new page** for the paper by adding a `paper-title.[md|html]` file in (./p)[./p]. Prefer `.md` for better linting. The file's structure is as seperated in metadata defined in yml format and custom html code split by `---`. Look at the existing `.md` and `.html` files for reference. Once you added the file, your page will automatically be available at `*url*/p/paper-title`.
3. **Add the new paper to the navigation** by adding its name and path to `_data/pages.yml`

# Delopying website

## Github Pages
The repository contains a github action that build and deploys the website to github pages. 

## Locally
You can generate the static files with
```bash
pixi run deploy --baseurl "https://your-url/optional-path"
```