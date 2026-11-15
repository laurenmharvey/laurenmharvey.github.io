# Lauren Michelle Harvey’s website

A two-page [Academic Pages](https://github.com/academicpages/academicpages.github.io) / Jekyll site for **https://lmharvey.com**. The site has a home page and a CV page with an embedded PDF. The theme supplies responsive navigation, the author profile, and light/dark appearance controls.

## Routine updates

| What to change | File |
| --- | --- |
| Short bio and research interests | `_pages/about.md` |
| Name, affiliation, email, ORCID | `_config.yml` |
| Headshot | `images/lauren-harvey.png` |
| CV (replace the PDF using the same filename) | `files/lauren-harvey-cv.pdf` |
| Home / CV menu | `_data/navigation.yml` |

On GitHub, open the file, click the pencil to edit, and commit the update. To replace the CV or portrait, use **Add file → Upload files**, keeping its filename unchanged. The site rebuilds after changes reach `main`. Leave `CNAME` as `lmharvey.com`.

## Accept this update (Lauren)

1. Open the pull request linked with this delivery while signed in as `laurenmharvey`.
2. Review **Files changed**, especially `_pages/about.md`, `_config.yml`, the headshot, and the PDF. Check that the **build** check passes.
3. In your repository, open **Settings → Pages** and select **GitHub Actions** as the build/deployment source. The included workflow builds Jekyll and deploys after merge; the fork does not deploy to your domain.
4. Click **Merge pull request**, then **Confirm merge**. If you want to revise the wording, those files can also be edited before merging.
5. In **Actions → Build and deploy site**, wait for the build and deploy jobs to finish. Visit **https://lmharvey.com** and check both Home and CV. If needed after changing the Pages setting, choose **Run workflow** on `main`.

The existing custom domain is preserved. No DNS change is required for this redesign.

## Local preview

With Ruby 3.3+ and Bundler installed:

```sh
bundle install
bundle exec jekyll serve --host 127.0.0.1
```

Open the Local URL printed by Jekyll. For a production build: `JEKYLL_ENV=production bundle exec jekyll build --strict_front_matter`.

## Theme maintenance

See [THEME.md](THEME.md) for upstream provenance and the small isolated customizations. Content lives in Markdown and YAML; there is no bespoke application framework or npm dependency tree. Only Home and CV are published as content pages; the theme’s demo pages and collections are not included. Some mobile browsers open PDFs in their own viewer; a direct PDF link is provided on Home and inside the embed’s fallback.
