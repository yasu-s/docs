# HTML5 APP CONFERENCE 2018  

## 基調講演 - Web App Platform Strategy  

* Mozilla Japan -> WebDINO JAPAN  
* Web vs App -> Web love App  
* Web標準
  * 最も知られている
  * ライブラリが豊富
* 最も採用されている技術  
  * JS,HTML,CSS,TypeScript上位に入ってくる  
  * F/W, Lib -> Node.js, Angular, Cordovaが上位に入ってくる  
* Web APPの歴史  
  * Firefox, Chromeの出現。
  * スマホの出現による低迷。
  * PWA登場によるWeb APP復活。
* HTML5は2018年３月終了。現行はHTML5.1
* HTML5, PWA, JS, WA
* アプリはよく使うもののみインストールする。
* 滞在時間の長いWebアプリでPWAが活用

## 開発・運用・チームビルディング  

* Ionic活用事例  
  * iframeの利用  
    * localStorageのオーバーライド:同一オリジンで複数データを管理するため  
  * 位置情報と連動したリアルタイム情報共有アプリ（メッセージ・画像・動画）  
    * 無限スクロールコントロール。１８０度回転させて利用（上下反転）  
* なぜHTML5アプリなのか  
  * コンパクトで流動的なチームをめざす  
    * 個々がが強くなる。技術の洗濯と集中  
      * モバイルアプリ：Ionic、Webアプリ：Angular
      * Webアプリ・モバイルアプリの両方に対応できる。  
      * 機械学習利用のため、バックエンドはpython利用  
      * ML Kit for Firebase -> localのモデルだけでML利用が可能  
      * Firebaseにバック・DB・インフラの統合を目指している
      * バックエンドはFirebase Functions（Node.js）を利用  
      * CRUD APIの作るコストが減った  
* Ionic, Angular, Firebase  
  * TypeScript/JavaScriptだけで対応できる
* 仕事の選択と集中
  * HTML5アプリなので、簡単なものはWEBブラウザでレビューできる。
  * circleci ->  dockerからイメージ取得 -> ビルド・デプロイ  
  * 顧客にURLを送り、Github上でレビューができる。  
* IT DART（災害時の情報支援団体）

## PWA, Cordova, Capacitor, ReactNative Dom  

* ハイブリッドアプリ戦国時代  
  * Xamarin：C#/MS  
  * React Native：JavaScriptをNativeに実行  
    * React Native for Web  
    * React Native DOM  
  * Cordova/PhoneGap：Webブラウザを利用してネイティブチックな画面にする。  
    * Ionic：UIフレームワーク
    * Onsen UI 2：UIフレームワーク
    * Monaca：開発エディタ、プラグインの利用が楽
  * Capacitor：Ionicチームが作成。ブラウザ・Android・iOS・Electron。
    * Native UI Shellが可能。(Native + Web Viewの融合)  
  * PWA：オフライン表示、バックグラウンドSync、Push通知、ホーム画面に追加。インストール不要。
  * デザインの表現力：Xamarin < Cordova。HTMLだとなんでもできる
  * 処理速度：ネイティブ < HTML5・Cordova
    * FPS60等のゲームを除き、処理速度に差はない。技術力次第でHTML5でも処理速度は早い。
　* Ionicの採用事例は増えている。
* Web製作者がアプリをつくる世界に  

## pixiv PWA  

* チャット形式の小説を投稿できるサービス
  * Android, PC -> PWA
  * iOSは Native
* PWAの特徴
  * オフライン通知、Push通知 etc  
* A2HS  
  * ホーム画面に追加　機能
  * Androidではアプリ扱い  
  * App Install Bannerがでる。
    * ２回以上にWEBサイトにアクセス、再訪に５分以上の間隔
* Lazy Load + Cache
  * Cache
    * Service Worker  
  * JS Lazy Load
    * chunk.jsで分割。必要な分だけ読み込む
  * 初期ロードは最初の画面分のリソースを読み込む
  * 初期ロードが終わるとほかのリソースをキャッシュ
  * キャッシュがおわるとオフラインで使用可能
  * オフラインからオンライン復帰時の再試行ができる
* マルチプラットフォーム対応  
  * 段階的拡大；ブラウザ対応を順次拡大
* アーキテクチャ  
  * Ionic3, Angular 5
    * Cordova部分は不採用
    * SSRできない
  * backend：Rails、MySQL
  * Firebase hosting
    * 静的ファイルのホスティング  
  * FIrebase functions
    * サーバー側で必要な軽いタスクを行う
  * AWS S3
  * CI
    * PR・レビュー
    * バグの場合、PWAはクラッシュせず静かに止まる
    * heroku Review Apps  
      * GithubでPRをつくると自動でアプリ生成。
      * herokuは静的ファイルを配置
    * RC版を毎日ビルド


## フロントエンドでクラウドをいい感じに使う  

* JSなWebアプリ（SPA）からAWSをいい感じに使う  
* 課題
  * サービスがたくさんあり使い方がわからない。
  * プロビショニングの仕方がわからない。
  * SDKの使い方がわからない
* AWS Amplify
  * フロントエンド・モバイル開発者向けオープンソースのJSライブラリ  
  * React, Angular, Vue.jsをサポート
  * できること  
    * Auth  
    * Analytics  
    * API  
      * Amazon Pinpoint, ターゲットされたプッシュ通知・キャンペーンのスケジューリング。ABテスト
      + AWS Lambda
    * GraphQLクライアント
    * Storage
      * S3連携
    * Push通知
    * Amazon Lexの利用
    * PubSub
    * Caching
    * i18n
  * Mobile Hub + Mobile CLIで設定可能  


## PWA/iOS/Android 対応のHTML5 アプリを実プロダクトでいかに構築し、育てていくか

* 技術選定
  * アプリ開発の種類
  * ハイブリッドアプリのオーバーヘッドが大きい。
    * Cordova plugin対応にタイムラグがあるなど。
  * 選定フローチャート
    * ネイティブアプリ
      * アニメーション
      * パフォーマンス
      * ネイティブ機能
      * iOS/Androidの開発者がいる
      * 予算期間がある
    * ハイブリッドアプリ
      * 技術者がいなく、予算期間がない。
  * Cordovaは導入コストは安く・運用コストは高い
* 開発環境
  * 静的型付けを推奨
  * チェックは厳しめにする
  * Live Reload/Hot Reload機能はほしい。最近のFWは大体もっている
  * 開発用・本番用のアプリを分ける。バンドルIDを分ける。
* 設計
  * ビジネスロジックの設計（Service）
    * Viewに依存しないようにする
    * フレームワークに依存しない層
    * 依存するものはControllerとしてServiceと別にする。
    * publicなIFは全てStream or Promiseを返す。
    * 後から非同期にするのは大変
    * async/awaitを使う
  * Presentational Components
    * Dumb component  
      * データを表示するだけ
    * Smart component
      * 複数制御
* テスト
  * UIテストは難しい  
  * 変更が頻繁におきるので、メンテナンスコストが高い
  * テスト対象を絞る
    * ビジネスロジックを中心
    * よくバグが出るところ
    * 致命的なところ
  * 構成：Karma + Jasmine + Chrome
  * 副作用としてテストしやすいコードを書くようになる
* ロギング
  * アプリケーションログ
  * 操作ログ
  * パフォーマンスログ
  * エラーログ
  * client logger
    * サーバーへの送信。圧縮・再送等をおこなっている
  * ログデータ
    * 端末ID、OS、アプリバージョン etc
* 監視
  * Mackerel, Newrelic, datadog etc
* 分析
  * Google Analytics
  * BigQuery


