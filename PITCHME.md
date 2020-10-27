# はじめての PostCSS

2020-09-28 @mmyoji

---

## Content

* autoprefixer-rails の話
* PostCSS とは
* 余談 - Sass
* Plugins
* How to use

---

## autoprefixer-rails の話

* CSS に vendor prefixes を付与する
* RoR 上で使う場合は Sprockets と連携して動作する
* 元メンテナ「こんな gem 使ってないで PostCSS の Autoprefixer plugin 直接使え」
* 新メンテナが現れて deprecation warning が消えてしまう

---

## [PostCSS](https://postcss.org/) とは

* JS で完結した CSS の transpiler
* 200以上ある Plugin を組み合わせて使う

---

## 余談 - Sass

* Sass は元々 Ruby で compile されていた
* 今は [LibSass](https://github.com/sass/libsass) という C++ 実装の compiler ができた
* 言語に応じて LibSass を利用するための bindings を使う
    * e.g., Ruby なら [sassc-ruby](https://github.com/sass/sassc-ruby), Node.js なら [node-sass](https://github.com/sass/node-sass)
* 2020-10-26 に [Sass: LibSass is Deprecated](https://sass-lang.com/blog/libsass-is-deprecated) が出て LibSass は deprecated になった
* これからは DartSass を使うように

---

## Popular Plugins

（※独断と偏見に基づく）

* [Autoprefixer](https://github.com/postcss/autoprefixer): vendor prefixes
* [Preset Env](https://github.com/csstools/postcss-preset-env): CSS版 babel 的なもの。CSS の最新機能を利用できる
* [Nested](https://github.com/postcss/postcss-nested): Sass-style nesting
* [stylefmt](https://github.com/morishitter/stylefmt): stylelint を元に format
* [cssnano](https://cssnano.co/): minifier

---

## How to use

* webpack example: https://github.com/postcss/postcss/tree/8.0.9#webpack
* CLI (w/ [postcss-cli](https://github.com/postcss/postcss-cli)): `postcss --use autoprefixer -o main.css css/*.css`

---

おわり
