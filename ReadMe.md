# このソフトウェアについて

Gulp環境構築する。

HTML(pug),CSS(stylus),JS(ES6..)の自動ビルド環境をつくる。

# 概要

メタ言語|出力言語
--------|--------
stylus|css
pug|html
ES6(webpack,babel)|js

# 使い方

## node_modules インストール

```sh
$ cd (このディレクトリ)
$ ./install.sh
```

* package.json
* node_modules/
* dst/

ファイルサイズ約92MB。所要時間約9分。[※](memo/install.md)

## 起動

```sh
$ cd (このディレクトリ)
$ gulp
```

* ビルド（ファイル結合, トランスパイル）
* ブラウザ起動

なお、pug,stylus,jsのソースコードが変更されるたびに自動でビルド＆ブラウザ更新される。

## gulp

```sh
$ cd (このディレクトリ)
$ gulp
```

### トランスパイル

* `./src/stylus/**/*.styl`→`./dst/css/*`
* `./src/pug/**/*.pug`→`./*`

詳細は[gulpfile.js](gulpfile.js)参照。

### 起動

ローカルサーバ、ブラウザ、が起動し、./index.htmlが表示される。

ローカルサーバはターミナルで`Ctrl+C`キー入力すれば停止できる。(Ctrl+Zで強制終了してしまうとプロセスが残ってしまう模様)[※](run.md)

# 実装時にハマったこと

vimでインデント設定してやらないとエラーになる。[※](memo/vim.md)

# 開発環境

2018-04-24時点。[※](memo/install.md)

* [Raspberry Pi](https://ja.wikipedia.org/wiki/Raspberry_Pi) 3 Model B
    * [Raspbian](https://www.raspberrypi.org/downloads/raspbian/) GNU/Linux 8.0 (jessie)
        * vim 7.4
        * Chromium 56.0.2924.84
        * Node.js 9.4.0
            * npm 5.6.0
                * n 2.1.7
                * Gulp 3.9.1
                    * work系
                        * gulp-plumber 1.2.0
                        * gulp-notify 3.2.0
                        * browser-sync 2.23.7
                    * HTML
                        * gulp-pug 4.0.1
                    * CSS
                        * gulp-stylus 2.7.0
                    * JS
                        * webpack 4.6.0
                        * webpack-stream 4.0.3
                        * gulp-babel 7.0.1
                        * babel 6.23.0
                        * babel-env 2.4.1
                        * babel-polyfill 6.26.0
                        * babel-preset-env 1.6.1



# ライセンス

このソフトウェアはCC0ライセンスである。

[![CC0](http://i.creativecommons.org/p/zero/1.0/88x31.png "CC0")](http://creativecommons.org/publicdomain/zero/1.0/deed.ja)

