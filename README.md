# Type

Type is an elegant, minimalistic Jekyll blogging theme based on [poole](https://github.com/poole/poole/tree/gh-pages). It focuses more on typographic style aesthetics, especially Chinese, Japanese, and Korean text content. As we all know, there is no perfect solution to the problem of CJK and English mixed typesetting at present, so it is inevitable that there will be some compromises in the design. In addition, it implements some fine-grained features and fixes some minor bugs of poole, which you can see below.

![English](/assets/README_en.png)

![Chinese](/assets/README_cn.png)

See Type in action with the demo [English typesetting](https://typesetting.vercel.app/2022/08/14/hamlet) / [Chinese typesetting](https://typesetting.vercel.app/2022/08/12/autumn/).

## Features
- Responsive Design
- RSS feed (link [here](https://typesetting.vercel.app/atom.xml))
- Math formula support (view in [example post](https://typesetting.vercel.app/2022/08/05/example/))
- Dark Mode (based on the system theme)
- [Archive](https://typesetting.vercel.app/archive), tags features (easy to add yourself)
- Rich html style support ([example content](https://typesetting.vercel.app/2022/08/05/example/))
- GitHub gist embed support and more...

## Usage

### 1. Quickly deploy on vercel

Clone this repository:
```bash
$ git clone git@github.com:livrth/type.git blog
```

All site titles, and personal information are modified in the `_config.yml` file, you can customize these content.

All blog posts are in the `_posts` directory, create your own here. Be sure to pay attention to the naming format, it needs to start with the date like the files I've put here.

Then you can use git to reinitialize this directory, create a new remote repository of your own, and just git push.

The last thing you need to do is to register an account on [vercel](https://vercel.app/), and then deploy the repository where you store this blog.


### 2. Deploy on GitHub Pages

Frankly speaking, in 2022 GitHub Pages still [do not support](https://github.com/github/pages-gem/issues/651) Jekyll 4.0 and newer version, which makes many new features unavailable. Rendering of mathematical formulas is a problem, MathJax renders fine in Jekyll 4.0 and later versions most of the time, but does not display properly in lower versions. If your blog contains a lot of mathematical formulas, I suggest you deploy it in vercel, because it supports Jekyll versions after 4.0.

But GitHub has recently [released](https://github.blog/changelog/2022-07-27-github-pages-custom-github-actions-workflows-beta/) new feature of deploying GitHub Pages using GitHub actions, which allows us to use Jekyll 4.0+ version.

I have already written the actions template and put it in the `.github` directory, so you only need to go to your repository's Settings -> Pages -> Build and deployment, and set the `Source` option to `GitHub Actions`. Note that you don't need to click the `configure` button, because the configuration file I have already written for you can be used directly.


## Local development or debugging
If you are not interested in developing the code for the blog itself, then you can ignore this part.
### 1. Install dependencies

Type is built on Jekyll and uses its built-in SCSS compiler to generate our CSS. Before getting started, you'll need to install the Jekyll gem:

```bash
$ gem install jekyll bundler
```
If you are unfamiliar with ruby, please refer to the official Jekyll installation [tutorial](https://jekyllrb.com/docs/installation/) and follow it step by step.

### 2. Running locally

Install all required gems:
```bash
$ bundle install
```
Preview the blog locally:
```bash
$ bundle exec jekyll serve --livereload
```
Depending on the version of Ruby and Jekyll on your system, there may be some warning messages, you can search Google to modify the version of these dependencies. Usually, however, these warnings have little effect.


## Credits
- [谈谈技术博客的排版 — ZHIX](https://zhix.co/posts/talking-typesetting/)
- [漢字標準格式 — 印刷品般的汉字排版框架](https://github.com/ethantw/Han/)
- [从《中文排版需求》开始 — The Type](https://www.thetype.com/2015/04/9171/)
- [Chinese copywriting guidelines for better written communication／中文文案排版指北](https://github.com/sparanoid/chinese-copywriting-guidelines/)
- [Requirements for Chinese Text Layout 中文排版需求](https://w3c.github.io/clreq/)
- [Understanding Minimalism](http://understandingminimalism.com/)
- [Hugo theme Purity](https://github.com/lingsamuel/purity)
- [Poole - The Jekyll Butler. A no frills responsive Jekyll blog theme](https://github.com/poole/poole)
- [Persephone - A minimal jekyll theme for building books and blog](https://github.com/erlzhang/jekyll-theme-persephone)

## License

Open sourced under the [MIT license](https://github.com/livrth/type/blob/master/LICENSE).