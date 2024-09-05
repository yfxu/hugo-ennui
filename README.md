# Ennui

Ennui is a simple hugo theme designed for personal websites. Ennui supports a simple landing page, blog posts, and a gallery page to share photos in an auto-scaling Google Photos-like album. The CSS and HTML used to implement the gallery is adapted from https://github.com/xieranmaya/blog/issues/6. The overall design is also pretty much a copy of the blog design used in https://rickrollblog.blogspot.com/.

This theme was made using Hugo version `0.121.0`, but may work with older versions as well.

# Customization

Add the following options to your `hugo.yaml` file (or TOML or JSON)

```yaml
theme: ennui
params:
  author:
    name: ""            # your name, which is displayed across the website
    stylizedName: ""    # stylized version of your name to be displayed across the website
  homePageSocials:
    - name: ""          # name of site/platform/service
      value: ""         # name of your account
      url: ""           # url to page
    - name: ""          # name of site/platform/service
      value: ""         # name of your account
      url: ""           # url to page
    - name: ""          # name of site/platform/service
      value: ""         # name of your account
      url: ""           # url to page
    - name: ""          # name of site/platform/service
      value: ""         # name of your account
      url: ""           # url to page
    # this array can be freely expanded/shortened, though it looks better with 4 links
title: ""               # Website title which is displayed on every tab
menus:
  main:
    - name: home
      pageRef: /
      weight: 1
    - name: about
      pageRef: /about
      weight: 2
    - name: blog
      pageRef: /posts
      weight: 3
    - name: photography
      pageRef: /gallery
      weight: 4
  footer:
    - name: ""          # name of site/platform/service
      url: ""           # name of your account
      weight: 1         # url to page
    - name: ""          # name of site/platform/service
      url: ""           # name of your account
      weight: 2         # url to page
    - name: ""          # name of site/platform/service
      url: ""           # name of your account
      weight: 3         # url to page
    # this array can be freely expanded/shortened, though it looks better with 3 links
```

You can also configure the colours displayed on the website in `assets/scss/_variables.scss`

```scss
:root {
  --color-background: #ffffff;
  --color-text-primary: #3b393d;
  --color-text-secondary: #a6a9ad;
  --color-accent: #45b694;
}

@media (prefers-color-scheme: dark) {
  :root {
    --color-background: #2B2A33;
    --color-text-primary: #ede3dd;
    --color-text-secondary: #747a7a;
    --color-accent: #03CEA4;
  }
}
```