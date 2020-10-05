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

#### Customizing the Jekyll Minima Theme
From the [Minima v2.5.1 docs](https://github.com/jekyll/minima/blob/v2.5.1/README.md):

> To override the default structure and style of minima, simply create the concerned directory at the root of your site, copy the file you wish to customize to that directory, and then edit the file.
e.g., to override the [`_includes/head.html `](_includes/head.html) file to specify a custom style path, create an `_includes` directory, copy `_includes/head.html` from minima gem folder to `<yoursite>/_includes` and start editing that file.

#### Debugging

**General**

If something doesn't update after changing, try stopping and restarting the local server.

**Finding the local Minima instance:**

To locate the instance of the `minima` theme's Ruby Gem on your machine do:

```bash
bundle show minima
```

That should output the path to the Minima Gem.

### Deploying

The site is deployed using [Netlify](https://netlify.com). 

When changes are made to the main branch of the repository Netlify will automatically rebuild and deploy the site. Additionally, any Pull Request made against the main branch will create a deploy that may be previewed prior to merging.
