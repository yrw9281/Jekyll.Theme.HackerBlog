# The Hacker-Blog theme

The theme of my blog is a modified version of the [hacker-blog](https://github.com/tocttou/hacker-blog) and [hacker-theme](https://github.com/pages-themes/hacker).

### Included

1. Pagination
2. SEO tags
3. Archive Page
4. Tags
5. About Page
6. RSS (`https://base-url/atom`)
7. Sitemap (`https://base-url/sitemap`)
8. Google Analytics (optional)

## Usage

1. Fork and Clone this repository
2. Customize your blog
3. Add a new post in `_posts/` directory with proper name format (as shown in placeholder posts)
4. Commit and push to master on a repository named `<githubusername.github.io>`.
5. Visit `<githubusername>.github.io`

## Local Build Using Docker

Quick build up the local environment and focus on the posts.

### Build image

```bash
docker build -t myBlog . 
```

### Docker run

```bash
docker run -p 4000:4000 -v .:/app myBlog
```

Visit `http://localhost:4000/` to access the blog.

## Customizing

### Configuration variables

Edit the `_config.yml` file and set the following variables:

```yml
title: [The title of your blog]
description: [A short description of your blog's purpose]
author:
  name: [Your name]
  email: [Your email address]
  url: [URL of your website]

baseurl: [The base url for this blog.]

paginate: [Number of posts in one paginated section (default: 3)]
owner: [Your name]
year: [Current Year]
```

*Note: All links in the site are prepended with `baseurl`. Default `baseurl` is `/`. Any other baseurl can be setup like `baseurl: /hacker-blog`, which makes the site available at `http://domain.name/hacker-blog`.*

Additionally, you may choose to set the following optional variables:

```yml
google_analytics: [Your Google Analytics tracking ID]
```

### About Page

Edit `about.md`

### Layout

If you would like to modify the site style:

**HTML**

Footer: Edit `_includes/footer.html`

Header: Edit `_includes/header.html`

Links in the header: Edit `_includes/links.html`

Meta tags, blog title display, and additional CSS: Edit `_includes/head.html`

Index page layout: Edit `_layouts/default.html`

Post layout: Edit `_layouts/post.html`

**CSS**

Site wide CSS: Edit `_sass/base.scss`

Custom CSS: Make `_sass/custom.scss` and use it. Then add `@import "custom";` to `css/main.scss`

**404 page**

Edit `404.md`

## License

CC0 1.0 Universal