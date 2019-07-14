# 概要

* https://ngjapan.org/

# keynote

## Angular community

* Scale OSS, New Collaborators

## V8

* v2-4 と比べるとupdateが楽に
* Differential Loading
  * Evergreen LegacyブラウザでPolyfillを異なる仕様
  * Evergreenは最小のPolyfill（41kb減らせる）
* Route dynamic imports
  * `import('').then`の記述ができる
  
## Ivy

* Smaller bundle
* Faster compilation
* Simpler debugging 
  * Breakpoints in HTML
  * Debuggable chnage Detection
* Improved type checking
* Backward compatible
* angular.io/guide/ivy
* Lower memory

## Bazel

* Scale on the Cloud
* @angular/bazel でpreview版使用可能

## Angular Components

* material -> components
* material-experimental で試せる
* TestbedHarnessEnvironment 
* angular/cdk-experimental/testingでてすとについてためせる

# Micro Front End Architecture with Framework agnostic Web Components

## Micro Frontend

* 

## Web Components

* HTML Import
* HTML Templates
* Custom Elements
* Shadow DOM

## Custom Elements

* React, Vue.js などもCustomElements in Framework

# Angular Elements under the hood

* Custom Elements APIでのJS実装
  * HTMLElementを継承してじっそう
  * connectedCallbackで接続
* Shadow DOM 
  * Componentで `encapsulation: ViewEncapsulation.ShadowDOM` を指定する
* Angular Elementsの内容をzone.jsに登録したい場合、最新版の場合は設定不要。（zone内でAngulae Elementsをdefineしているばあい）
* Scoped Zone

# Angular generic forms

* ControlValueAccesorの実装について

# Angular build, polyfills and application size

* Compression
  * GZip
  * Brotli - GZipより圧縮効率がよい
* Tree shaking
* AoT Compilation
* Code splitting
* Preloading lazy modlues
* Conditional polyfills 

# CapacitorをつかってAngularアプリの可能性を広げよう

* WebView onlyのアプリ + Native Functionsの呼び出し可能
* CapacitorはCordovaプラグインの使用可能
* npm publishで公開可能

# Black Holes and Angular Interceptors

* Interceptorのはなし

# Angularでメトロノームを作った話と、 Angular + pixi JSでメトロノームにオープニングをつけた話

# First step to Mobile x Angular @ the begining of 2019

* Cordova でアプリを作成
* OnsenUI or Ionic
* Monacaで開発

# AzureDevOps × BrowserStack × Angular

* Protractor＋BrowserStackで自動テスト
* BrowserStack
  * ブラウザバージョンが豊富
  * 動作中の動画が取れる
  * console.logなどとれる

# NestJS + TypeORM + Angularで作るPure TypeScriptなアーキテクチャ

* Ionic4 でWebComponentベースになった
  * Angular Routerをつかうようになった
  * ３からの移行は大変
* バックエンドもTypeScript
  * _legacyフォルダにして古い技術的負債は移動
* TypeORM - ORマッパー
* monorepoという選択肢
  * １リポジトリで複数モジュール
  * Lerna 
* Greenkeeperのような機能あり

# Building a Fast & SEO Friendly SPA with Angular

* SPA, Firebase Hosting, NoDB(JSON)
* SEO
  * meta tag
  * robots.txt は環境ごとにfileReplacements
* Rerendering during build time
* Puppeteer
  * Programmable Chrome Browser
  * html file generate
* prerender-spa-plugin
* generate sitemap - create-file-webpack
* husky - hook
* SVGOMG
* webp（静止画ファイルフォーマット）
* font import

