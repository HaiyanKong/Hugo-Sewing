# <div align="center">Hugo-Sewing</div>

<div align="center">

![Static Badge](https://img.shields.io/badge/license-MIT-blue.svg)

[Demo site](https://haiyankong.github.io/hugo-sewing-demo/)

</div>

Hugo-Sewing is a simple, clean and flexible Hugo theme for both personal blog, group website, and academic website. 

## Screenshots

>  Made by [everysize](https://everysize.kibalabs.com/)

![homeScreenshot](./static/readme/screenshot.png)

## Background

Hugo-Sewing is heavily based on [Hugo-Xmin](https://github.com/yihui/hugo-xmin), with modifications mainly inspired by [Shayan Hosseini's website](https://github.com/shayanh), [Hugo-Astatine-Theme](https://github.com/hugcis/hugo-astatine-theme), and [Hugo-Holy](https://github.com/serkodev/holy):

- The base of Hugo-ht is [Yihui Xie](https://github.com/yihui)'s [Hugo-Xmin](https://github.com/yihui/hugo-xmin).

- The academic layout ("Home", "Project", "Publication", and "People") is modified the code from [Shayan Hosseini's website](http://shayanh.com/) by [Shayan Hosseini](https://github.com/shayanh) and [Hugo-Astatine-Theme](https://github.com/hugcis/hugo-astatine-theme) by [Hugo Cisneros](https://hugocisneros.com/)

- The visual styles (navigation, index list, and footer) based on the [Hugo-Holy](https://github.com/serkodev/holy) theme by [SerKo](https://serko.dev/).

- Markdown style based on [Hugo-HT](https://github.com/hongtaoh/hugo-ht) theme by [Hongtao Hao](https://hongtaoh.com/).

- Shortcode ported from: [tutorial](https://www.sleepymoon.cyou/2023/hugo-shortcodes/) by [https://www.sleepymoon.cyou/](https://www.sleepymoon.cyou/) and [tutorial](https://fourxiajiao.github.io/2022/hugo-blog/) by [https://fourxiajiao.github.io/](https://fourxiajiao.github.io/).

- Toc style ported from: [tutorial](https://www.sulvblog.cn/posts/blog/hugo_toc_side/) by [Kevin Xu](https://www.sulvblog.cn/).

- Memos page ported from [memos.top](https://github.com/eallion/memos.top) by [eallion](https://www.eallion.com/).

- ......

This amalgamation of influences led to the name "Hugo-Sewing," symbolizing the process of intricately stitching together these diverse elements to create a cohesive theme.

## Features

- Includes various shortcodes to meet diverse needs, more detais can see this [Blog](https://haiyankong.github.io/hugo-sewing-demo/blog/2024/05/hugo-sewing-shortcodes/).
- Mobile-friendly and widescreen-friendly designs.
- Supports the integration of the [Giscus](https://giscus.app/) comment system, powered by [GitHub Discussions](https://docs.github.com/en/discussions).
- Academic style: with publication, project, and people Page.
- Utilizes the [Memos](https://github.com/usememos/memos) system for the "Memos" page, allowing to post personal moments, group galleries, and news.
- "Contact" page features the comment system and enables easy addition of map images.

## Installation

> Note: If you encounter a "443: Timed out" error when using either method, it's likely due to internet connectivity issues. In that case, you can download the repository and place the `hugo-sewing` folder inside the `themes` directory. Then, simply copy the files from `hugo-sewing/exampleSite` to the root folder and run `hugo server -D`.

### Direct Clone

```
hugo new site demosite
cd demosite/themes
git clone https://github.com/HaiyanKong/hugo-sewing
cd ..
cp -r themes/hugo-sewing/exampleSite/* .
```

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
git submodule add https://github.com/HaiyanKong/hugo-sewing.git themes/hugo-sewing
cp -r themes/hugo-sewing/exampleSite/* .
```

```
hugo server -D
```
Then, open `http://localhost:1313/`, then you will see the website like the [demo site](https://haiyankong.github.io/hugo-sewing-demo/).

#### Update with submodule

```
cd themes/hugo-sewing
git checkout main && git pull
cd ..
git add hugo-sewing
git commit -m "updating submodule to latest"
cd ..
```
> The above code copied from [hongtaoh](https://github.com/hongtaoh)/[hugo-ht](https://github.com/hongtaoh/hugo-ht)
> The difference between two methods:
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
- [How to Build a Website Using Hugo without Programming Skills](https://hongtaoh.com/en/2020/06/05/get-started-with-hugo/)
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
│  │  │      
│  │  ├─blog
│  │  │      
│  │  ├─people
│  │  │      
│  │  └─project
│  │          
│  └─static
│      ├─blog
│      │      
│      ├─contact
│      │      
│      ├─info
│      │      
│      ├─people
│      │      
│      ├─project
│      │      
│      └─publication
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
│  │      
│  ├─shortcodes
│  │      
│  └─_default
│          
└─static
    ├─css
    │      fonts.css
    │      style.css
    │      
    └─readme
```