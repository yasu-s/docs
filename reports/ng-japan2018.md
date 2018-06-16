# ng-japan 2018

## Keynote

### moment  

* tokyo meetup coming soon  
* datapicker header Custom(Angular Material)  
  * calendarHeadeComponent binding  

### 6.0.0  

* stability + innovation  
* ng update  
  * @angular/core, rxjs, typescript  
  * thirdparty library.  
  * migration schematics.  
* ng add  
  * ng add @angular/material  
    * package.json書き換え  
    * import appmodule  
    * theme, icons font追加される。  
* Angular library and other  
  * Material  
  * Elements  
  * PWA  
  * bootstrap  
* Tree shakable providers  
  * inject関連
* Angular Elements  
  * custom elements define  
* Angular Material  
  * Tree  
    * Nested tree DOM  
    * Flat tree DOM  
  * Form Field  
    * Fill from, outline  
  * Table  
  * Badge Button Sheet  
  * New layout algorithm for overlay  
  * cdk package text-field  

### Future  

* Project Ivy  
  * rendering  pipeline  
  * smaller/Faster/Simpler  
  * Ivy + Angular Elements  
  * React, jQuery -> Angular Elements 呼び出し
* Material & CDK  
  * CDK  
    * Listbox & combobox  
    * Datepicker  
    * Slider  
    * virtual Scrolling（仮想化）

## Angular PWA

### UXから観たPWA  

* PC,モバイルの違い  
  * PC -> タブが横、モバイル：タブが縦
* キャッシュをユーザーに近いところ ->　アプリキャッシュ  
  * Service Workers + Cache API  
  * オフラインレスポンス  
* Push Notification  
* installできるデバイスが増えている  
  * モバイル、PCにインストール可能  

### AngularのPWA  

* @angular/service-worker
  * 実行モジュール  
  * workerすくりぷと　
* @angular/pwa
  * コード生成補助  
  * manifest.json生成  
  * service-workerのインストール・コード追加  
* Angular側にswUpdate, swPushが追加  
* APIサーバーとのバージョンずれについて  
* ng build 時にキャッシュリソース
* strategy  
  * cache first  
    * キャッシュ優先。期限切れなら通信する  
  * network first  
    * ネットワーク優先  
* キャッシュの更新通知  
* LazyLoading ->かつあい  

### これからどうなるか  

* better web app  
  * AngularならserviceWorkerをひっそりバックグラウンドで動かすだけでも恩恵あり  
  * Installable AppはiPhoneがおいついていない
* Ivy + Elements = Web Components  
  * フルクライアントからマッシュアップになっていく  
* オフラインアプリの可能性  
  * 現状、background-syncがアプリ起動中でないとうごかない  


## Angular活用実績  

* Javaの技術者が多く、フロントエンジニアが少ない  
* 標準化が大変  
* オフショア教育  
  * Promiseの動き  
  * Java技術者にTypeScriptはわかりやすい  
* メモリリークとの戦い  
  * SPAを立ち上げたまま長時間利用 -> ブラウザのメモリ使用量増加  
  * 対策  
    * SPA分割。  
      * 業務完了時に再リロードさせる  
    * リークしそうな箇所を局所化  
      * evebt, subscribe, webstrage, DOMリーク
      * サードパーティライブラリはSPA前提でないのでリークしやすい  
      * ngondestroyで解放する

## NHKでの取り組み  

* NHKでのアーキテクチャについて  
  * Angular / Firebase / Cloud Fire Store  
  * インフラを別のところにおいている。セキュリティ的にきびしいため  
* Realtime AR  
  * XR  
    * VR, AR, MR = XR  
  * レインテンシーが悪い　　
  * XR <=20msが理想  
  * 5G <= ms  
* Angular + WebVR  
  * Angular6からWebVRと別々のものにできる  

## screenshot Test  

* 画像を比較してUIテスト  
* 前のUI画像を保存して、現在UIを比較  
* ３つのつーる
  * Storybook
  * Puppeteer -> ヘッドレスブラウザ  
  * reg-suit -> Commit履歴から画像比較  

## protractor  

* protractorようのWebDriverがある  

## Angular PlantUML  

## CSS設計手法
* AngularのCSS
  * Component CSS  
    * クラスのみに影響  
    * このCSSだけでアプリケーションを構成できると良い。  
  * Shared CSS  
    * 複数のクラスから読み込まれるCSS  
  * Global CSS  
    * 全コンポーネントに対して影響  
    * style.cssで定義  

* 値の共通化  
  * Sassを利用する。  
  * 変数化する。色やpaddingsize etc  

## Angular CDK  

* CDK  
  * Component Behaviors  
  * Common Utilities  
* FocusMonitor  

## Angular ivy  

* Angular 4-6 pipeline  
  * template html -> template data -> Angular interpreter -> DOM  
* Ivy pipeline  
  * template html -> Template instructures -> DOM  
