# HET Website

The HET Website is a static site that provides content and marketing related materials for the SHLI Health Equity Tracker.

## Developer Notes

This site runs on the [Jekyll](https://jekyllrb.com) static site generator with the [Minima Theme](https://github.com/jekyll/minima).

### Install

To run the site locally you'll need to have the following installed on your machine: 

- Ruby >= @2.7.1
- Ruby Gems: bundler, jekyll

To manage Ruby versions it's recommended to use [rbenv](https://github.com/rbenv/rbenv#installation) and not the system Ruby on your machine.

After installing Ruby do:

```bash
gem install jekyll bundler
```

### Develop

Run the site locally by doing:

```bash
bundle exec jekyll serve --livereload --incremental
```

Note that the `--incremental` flag is an experimental feature which only builds parts of the site that have changed. It may need to be excluded when encountering build problems.

For any changes to `_config.yml` to affect the build process, you will need to stop and restart the build command above.

### Deploying

The site is deployed using [Netlify](https://netlify.com). 

When changes are made to the main branch of the repository Netlify will automatically rebuild and deploy the site. Additionally, any Pull Request made against the main branch will create a deploy that may be previewed prior to merging.
