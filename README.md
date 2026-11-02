# hmadrigal.github.io

Tech, personal and pet-project blog, published at <https://hmadrigal.github.io>.

Built with [Jekyll](https://jekyllrb.com/) and the [Chirpy](https://github.com/cotes2020/jekyll-theme-chirpy) theme. Pushing to `main` builds the site and deploys it to GitHub Pages through [`.github/workflows/pages-deploy.yml`](.github/workflows/pages-deploy.yml).

## Where things live

| To change                       | Edit                                 |
| ------------------------------- | ------------------------------------ |
| Blog posts                      | `_posts/YYYY-MM-DD-some-title.md`    |
| About page                      | `_tabs/about.md`                     |
| Title, avatar, social links     | `_config.yml`                        |
| Sidebar contact icons           | `_data/contact.yml`                  |
| Post share buttons              | `_data/share.yml`                    |
| Images                          | `assets/img/`                        |

## Writing a post

Create `_posts/2026-11-02-my-first-post.md`:

```markdown
---
title: My first post
date: 2026-11-02 10:00:00 -0600
categories: [Pet projects, Tools]
tags: [jekyll]
---

Write the post here in Markdown.
```

A post dated in the future is not published until a build runs after that date. See the theme's guide on [writing a new post](https://chirpy.cotes.page/posts/write-a-new-post/) and its [text and typography](https://chirpy.cotes.page/posts/text-and-typography/) samples.

## Previewing locally

Previewing is optional: a push to `main` is all it takes to publish. Either option below serves the site at <http://127.0.0.1:4000> and rebuilds when a file is saved.

**VS Code with Docker Desktop.** Open the folder, choose **Reopen in Container**, then run the **Run Jekyll Server** task (<kbd>Ctrl</kbd>+<kbd>Shift</kbd>+<kbd>B</kbd>).

**Docker from a terminal:**

```shell
docker run --rm -it -p 4000:4000 -p 35729:35729 -v "${PWD}:/site" -v hmadrigal-blog-gems:/usr/local/bundle -w /site ruby:3.4 sh -c "bundle install && bundle exec jekyll serve -H 0.0.0.0 -l --force_polling"
```

## Publishing

```shell
git add .
git commit -m "Add my first post"
git push
```

Progress shows up in the repository's [Actions tab](https://github.com/hmadrigal/hmadrigal.github.io/actions). A failed build leaves the live site as it was.

## Updating the theme

The theme comes from the `jekyll-theme-chirpy` gem, pinned in `Gemfile`. Files such as `_config.yml` and the workflow come from [chirpy-starter](https://github.com/cotes2020/chirpy-starter), so compare against that repository on a major version bump.

## License

Published under the [MIT](LICENSE) license.
