# HTML5 Conference 2018

## 概要

* 2018年11月25日（日）東京電機大学 千住キャンパス
* https://events.html5j.org/conference/2018/11/

## それ、AMPで作りませんか？

* amp-install-sw PWA対応
* manifest追加できる
* AMPキャッシュをのこしつつ、URLをふつうのものにする。（現状はgoogle.comとかがつく）
Singed Excahnge -> Preview版
* WorkerDOM でJSを動かす。WorkerThread上でReact Componentを動かせたりできる。

## TechFeedのつくりかた 2018

* Cordova + Angular
  * Ionic/Angular/Cordova, Webpack build.
  * Angular
    * 型付、リリースサイクル固定、CLI
    * マイグレーションが親切
    * アーキテクチャで迷うひつようなし
    * 学習コスト高、コンポーネント開発が重量感
  * Ionic
    * Ionic4でWeb Componentベースになる予定。なかなかでない。
  * UIフレームワークのジレンマ
    * デザイン部分ではエンジニア主導では良いが、デザイナーにとっては自由度が制限される。
    * デザイン段階でコンポーネント化すべき
  * Cordova
    * ゆらぎやすい基盤
    * プラグインの質がバラバラ
    * XCode, Android Studioのバージョンアップでビルドが上手くいかず
* Server side TypeScript
  * 旧基盤
    * Node.js 8
    * Loopback
    * モノリシック
  * 新基盤
    * NestJS
      * Angular like
      * decoratorベース。Javaっぽい感じ
      * DI, バリデーターなども可能
    * TypeORM
      * TypeSCriptベースのORマッパー
      * decoratorベース
    * Client/ServerともにTypeScript
* monorepo
  * モノリシックをモジュール化
  * 1リポジトリで複数モジュールを管理
  * Lerna
    * 複数モジュールの依存性を一括管理
    * 一括公開
    * リンク
* 経営をエンジニアリングする
  * clasp
    * Google Apps Scriptをローカル開発
    * Git
    * TypeScript使える
  * 経営用ダッシュボードをTypeScriptで作る

## Angular Webアプリケーション最新設計手法

* Component Design
  * Component - based Architecture
  * 良いComponentせっけいさえあれば、複雑な設計は必要でない
  * ４つにComponentを分類
    * App：トップレベル。Applicationそのものを表す
    * Page：URL単位
    * Container：状態管理を行う
    * Presentational：状態をもたない、表示専用
  * App Component
    * アプリケーション全体の設定、初期化
  * Page Component
    * 1URLにつき、1 Page Component
    * ここでRouter処理は行う
    * 再利用はしない
  * Container Component
    * 状態管理を行う
    * ServiceとPresentational Componentのデータの受け渡しに専念、ロジックを持たせない
    * 表示についてはPresentational Componentで行う
    * 複雑にならないよう、Serviceに処理を寄せる
    * Serviceに対してのメソッドコールをユニットテスト
  * Presentational Component
    * 状態を持たない。 (Serviceを使用せず)
    * Input, Outputのみ。
    * Container ComponentにOutputで伝搬
    * Input/Outputが適切に処理されているかユニットテスト
* Module Structure
  * Module has Components
  * Module は機能単位でのComponent の集合
  * Component群のカプセル化
  * ツリー構造をもつ
    * App Module, Feature Module
    * Feature Moduleはそれだけで完結する機能単位で分割
  * 大規模になる場合、機能ごとにFeature Moduleが必要
  * Core Module：Serviceや関数の共通化
  * Shared Module：ComponentなどView部分の共通化
  * feature-modulesフォルダ内に機能単位でフォルダを作成する
    * 上の階層からimportしない
    * 単独で動く
* State Management
  * Component と Serviceの連携方法
  * ２種類
    * Single Data Service
    * Global Store
  * Single Data Service
    * １つのデータタイプに１つのSerivce。複数のデータは持たない
    * データはStreamで提供
    * 小規模なアプリケーションで使用。スピードの求められる開発
  * Global Store
    * Reduxパターン
    * １つのStoreでデータを管理
    * NgRxを推奨
    * 決まった形式で統一的な実装が可能
    * どのActionがどの状態を変更するか分かりづらい
    * 小規模なアプリケーションに対しては複雑
    * Action Design
      * Storeの直接の更新はさせない
      * Action / Reducer は、 Storeに対しての更新クエリ。

## React におけるパフォーマンスチューニング

* ユーザーの入力に迅速に対応する
* AirSHIFT
  * シフト表が直感的に作れる
  * React/ Redux + BFF(redux-pluto)
  * Component 600個
* スクリプティングが遅い
  * Scriptingの詳細を調査
  * React内部で何が起こっているか
  * Chrome DevTools
  * React DevToolsのHigligt Update, Profiler, User Timing で調査
  * User Timing API. 
  * 操作とComponentレンダリングの関係性がわからない
  * redux-action-timing-middleware
* 改善のアプローチ
  * 処理時間をへらす
    * 関数の処理時間を短くする
    * メモ化（memoize）
  * 無駄な処理をしない
    * 呼ぶ必要のない関数を呼ばない
    * 設計レベルの見直しが必要な場合も
    * Reconciliation
      * 仮想DOM
      * shouldComponentUpdate
      * 差分レンダリングが必要か判定
      * 木構造を減らす
      * shouldComponentUpdateを書く
    * React-Virtualized
      * 無限スクロール、仮想スクロールができる
      * 描画範囲内のDOM生成、描画範囲外は生成しない
    * Componentを小さく分ける
* DevTool
  * 低速モードで動かす（回線、スロットル）
* shouldComponentUpdateを楽に実装する
  * React.memo
  * PureComponent
  * shallowEqualで比較。
