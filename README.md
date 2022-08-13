# Type
Just like the [Hyde](https://github.com/poole/hyde) theme, [Poole](https://github.com/poole/poole/tree/gh-pages) is an elegant, classic, minimalistic Jekyll blogging theme, but it hasn't been updated in a long time, and it has some minor bugs and missing features. So I made minor modifications based on it to make the Chinese typesetting more beautiful, added support for mathematical formulas, and fixed some minor bugs.

![image](/assets/README.png)

See Type in action with the [demo site](https://typesetting.vercel.app/).

## Features
- Responsive Design
- Math formula support
- Dark Mode (based on the system theme)
- Archiving, tagging  features (easy to add yourself)
- Rich html style support ([example content](https://typesetting.vercel.app/page4))
- GitHub gist embed support and more...

## Usage

### 1. Quickly deploy on vercel
Clone this repository
```bash
$ git clone git@github.com:livrth/type.git blog
```
Go to the blog directory:
```bash
$ cd blog
```
All site titles, and personal information are modified in the `_config.yml` file, you can customize these content.

All blog posts are in the `_posts` directory, create your own here. Be sure to pay attention to the naming format, it needs to start with the date like the files I've put here.

Then you can use git to reinitialize this directory, create a new remote repository of your own, and just git push.

The last thing you need to do is to register an account on [vercel](https://vercel.app/), and then deploy the repository where you store this blog.


### 2. Deploy on GitHub pages

Frankly speaking, in 2022 GitHub pages still [do not support](https://github.com/github/pages-gem/issues/651) Jekyll 4.0 and newer version, which makes many new features unavailable. Rendering of mathematical formulas is a problem, MathJax renders fine in Jekyll 4.0 and later versions most of the time, but does not display properly in lower versions. If your blog contains a lot of mathematical formulas, I suggest you deploy it in vercel, because it supports Jekyll versions after 4.0.

Deploying on GitHub pages just requires adding GitHub actions. Copy all the files of the `.github` folder of the [repository](https://github.com/poole/poole/tree/gh-pages) where Poole is located to your own blog directory, and then push it to GitHub. If you also want good rendering of mathematical formulas on GitHub pages, I recommend taking a look at [KaTeX](https://katex.org/).



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

- [Poole - The Jekyll Butler. A no frills responsive Jekyll blog theme.](https://github.com/poole/poole)
- [Persephone - A minimal jekyll theme for building books and blog.](https://github.com/erlzhang/jekyll-theme-persephone)

## License

Open sourced under the [MIT license](https://opensource.org/licenses/MIT).