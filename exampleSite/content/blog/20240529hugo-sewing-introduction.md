---
title: "Hugo-Sewing Introduction"
date: 2024-05-29
author: Your Name
slug: hugo-sewing-introduction
draft: false
categories:
  - Hugo-Sewing
---

Hugo-Sewing is a simple, clean and flexible Hugo theme for both personal blog, group website, and academic website. 

![Static Badge](https://img.shields.io/badge/license-MIT-blue.svg)

[Demo site](https://haiyankong.github.io/hugo-sewing-demo/)

## Background

Hugo-Sewing is heavily based on [Hugo-Xmin](https://github.com/yihui/hugo-xmin), with modifications mainly inspired by [Shayan Hosseini's website](https://github.com/shayanh) and [Hugo-Holy](https://github.com/serkodev/holy):

- The base of Hugo-ht is [Yihui Xie](https://github.com/yihui)'s [Hugo-Xmin](https://github.com/yihui/hugo-xmin).

- The academic layout ("Home", "Project", "Publication", and "People") is modified the code from [Shayan Hosseini's website](https://github.com/shayanh).

- The visual styles (navigation, index list, and footer) based on the [Hugo-Holy](https://github.com/serkodev/holy) theme by [SerKo](https://serko.dev/).

- Markdown style based on [Hugo-HT](https://github.com/hongtaoh/hugo-ht) theme by [Hongtao Hao](https://hongtaoh.com/).

- Shortcode ported from: [tutorial](https://www.sleepymoon.cyou/2023/hugo-shortcodes/) by [眠于水月间](https://www.sleepymoon.cyou/) and [tutorial](https://fourxiajiao.github.io/2022/hugo-blog/) by [一笼虾饺有四个](https://fourxiajiao.github.io/).

- Toc style ported from: [tutorial](https://www.sulvblog.cn/posts/blog/hugo_toc_side/) by [Kevin Xu](https://www.sulvblog.cn/).

- ......

This amalgamation of influences led to the name "Hugo-Sewing," symbolizing the process of intricately stitching together these diverse elements to create a cohesive theme.

## Features

- Includes various shortcodes to meet diverse needs, more detais can see the [demo site](https://haiyankong.github.io/hugo-sewing-demo/).
- Mobile-friendly and widescreen-friendly designs.
- Supports the integration of the [Giscus](https://giscus.app/) comment system, powered by [GitHub Discussions](https://docs.github.com/en/discussions).
- The "Home" page boasts a customizable academic style, making customization.
- The "CV" page displays your resume or Curriculum Vitae directly and is downloadable.
- On the "Projects" page, your projects are showcased directly, with detailed information available upon clicking.
- The "Publications" page lists your publications and allows for easy addition of button links.
- The "People" page conveniently displays your group members and provides additional details upon clicking.
- Utilizes the [Memos](https://github.com/usememos/memos) system for the "Memos" page, allowing you to post personal moments, group galleries, or news.
- The "Contact" page features a comment system and enables easy addition of map images.

## Installation

> Note: If you encounter a "443: Timed out" error when using either method, it's likely due to internet connectivity issues. In that case, you can download the repository and place the `hugo-sewing` folder inside the `themes` directory. Then, simply copy the files from `hugo-sewing/exampleSite` to the root folder and run `hugo server -D`.

### Direct Clone

```
hugo new site demosite
cd demosite/themes
git clone https://github.com/user/hugo-sewing
cd ..
cp -r themes/hugo-sewing/exampleSite/* .
```

#### Deploy

```
hugo server -D
```
Then, open `http://localhost:1313/`, then you will see the website like the [demo site](https://haiyankong.github.io/hugo-sewing-demo/).

### Submodule

You can also add hugo-sewing as a submodule:

```
hugo new site demosite
cd demosite
git init
git submodule add https://github.com/user/hugo-sewing themes/hugo-sewing
cp -r themes/hugo-sewing/exampleSite/* .
```

#### Deploy

```
hugo server -D
```
Then, open `http://localhost:1313/`, then you will see the website like the [demo site](https://haiyankong.github.io/hugo-sewing-demo/).

> The difference between two methods (Copied from [hongtaoh](https://github.com/hongtaoh)/[hugo-ht](https://github.com/hongtaoh/hugo-ht)):
>
> If you add it as a submodule, the `hugo-sewing` theme you use is connected to this repository. The benefit is that you can keep it updated, but there is a caveat: if you make lots of changes to the styles based on your personal preferences, these changes might be lost.
>
> Simply `git clone` is recommended if:
>
> - You pretty satisfied with the current version of `hugo-sewing`; and/or
> - You are going to make changes according to your personal taste; and/or
> - You are not familiar with Git and do not know how to update the submodule.
>
> To update the submodule, run the following codes at the root directory of your hugo project:
>
> ```
> cd themes/hugo-ht
> git checkout main && git pull
> cd ..
> git add hugo-ht
> git commit -m "updating submodule to latest"
> cd ..
> ```
>
> The above codes came from [paularmstrong](https://github.com/tj/git-extras/pull/80#issuecomment-3992323).

## Excellent Hugo website building tutorials

- [How to Deploy A Hugo Website Using GitHub Pages Action](https://hongtaoh.com/en/2021/04/05/hugo-deploy-github-actions/)
- [Create and host a blog with Hugo and GitHub Pages in less than 30 minutes](https://www.mytechramblings.com/posts/create-a-website-with-hugo-and-gh/)
- [Blogging With Hugo](https://digitaldrummerj.me/series/blogging-with-hugo/)


## Folder Structure

```
.
│  .gitignore
│  LICENSE
│  README.md
│  theme.toml
│  
├─archetypes
│  └─default.md
│      
├─assets
│      
├─exampleSite
│  │  config.toml
│  │  
│  ├─content
│  │  │  contact.md
│  │  │  cv.md
│  │  │  memos.md
│  │  │  publication.md
│  │  │  _index.md
│  │  │  
│  │  ├─archive
│  │  │      people.md
│  │  │      project.md
│  │  │      
│  │  ├─blog
│  │  │      20240528hugo-sewing-markdown-style.md
│  │  │      20240528hugo-sewing-shortcodes.md
│  │  │      _index.md
│  │  │      
│  │  ├─people
│  │  │      people1.md
│  │  │      people2.md
│  │  │      people3.md
│  │  │      _index.md
│  │  │      
│  │  └─project
│  │          project1.md
│  │          project2.md
│  │          project3.md
│  │          _index.md
│  │          
│  └─static
│      ├─blog
│      │      hugo-sewing.pdf
│      │      hugo-sewing1.jpg
│      │      hugo-sewing2.jpg
│      │      hugo-sewing3.jpg
│      │      
│      ├─contact
│      │      findme.png
│      │      
│      ├─info
│      │      cv.pdf
│      │      profile.png
│      │      
│      ├─people
│      │      people.png
│      │      
│      ├─project
│      │      project.pdf
│      │      project.png
│      │      
│      └─publication
│              publication.pdf
│              publication.png
│              
├─i18n
│      en.yaml
│      zh.yaml
│      
├─layouts
│  │  404.html
│  │  index.html
│  │  
│  ├─partials
│  │      comment.html
│  │      footer.html
│  │      foot_custom.html
│  │      header.html
│  │      head_custom.html
│  │      memo.html
│  │      toc.html
│  │      
│  ├─shortcodes
│  │      abbr.html
│  │      align.html
│  │      blockquote.html
│  │      gallery.html
│  │      imgloop.html
│  │      mark.html
│  │      netease.html
│  │      pdf.html
│  │      spotify.html
│  │      timeline.html
│  │      toggle.html
│  │      
│  └─_default
│          contact.html
│          item-list.html
│          item.html
│          list.html
│          memos.html
│          single-simple.html
│          single.html
│          terms.html
│          
└─static
    ├─css
    │      fonts.css
    │      style.css
    │      
    └─readme
            blogScreenshot.png
            contactScreenshot.png
            cvScreenshot.png
            homeScreenshot.png
            memosScreenshot.png
            peopleScreenshot.png
            postScreenshot.png
            projectScreenshot.png
            publicationScreenshot.png
```