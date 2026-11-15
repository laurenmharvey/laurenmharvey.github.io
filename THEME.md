# Theme provenance

This site uses [Academic Pages](https://github.com/academicpages/academicpages.github.io), based on Minimal Mistakes, under the MIT license in LICENSE-ACADEMICPAGES.

Imported upstream revision: `8c57e1ae5da379512eb11165257fba02664b8531`.

The theme’s `_includes/`, `_layouts/`, `_sass/`, JavaScript, fonts, and icons are retained. Demo pages, collections, sample documents, notebooks, and template administration workflows are omitted.

Local presentation changes are isolated in `assets/css/custom.scss` (teal masthead, readable dark-mode links, a footer that stays below the content, focus outlines, portrait sizing, and the full-height CV embed). `_layouts/default.html` adds a page body class and optional footer suppression. `_includes/head/custom.html` loads the custom stylesheet. `_includes/masthead.html` labels the mobile menu button for screen readers. `_includes/author-profile.html` removes the Follow button; mobile contact links remain visible through the custom stylesheet. `_includes/footer.html` removes the link to the unused sitemap page.

The standard Academic Pages JavaScript bundle is committed as `assets/js/main.min.js`, so routine updates need only Jekyll. Regenerate it only when upgrading the theme’s JavaScript, using the upstream command:

```sh
npx --yes --package=uglify-js@3.19.3 uglifyjs assets/js/plugins/jquery.greedy-navigation.js assets/js/_main.js assets/js/theme.js -c -m -o assets/js/main.min.js
```

When updating the theme, compare upstream changes in these files rather than overwriting Lauren’s content and configuration. Retain both license files.
