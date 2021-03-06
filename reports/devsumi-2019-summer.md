# DevSumi 2019 Summer

## B-4 組織にテストを書く文化を根付かせる戦略と戦術

### 概要

* 13:15～14:00
* 和田 卓人氏[タワーズ・クエスト]
* https://speakerdeck.com/twada/strategy-and-tactics-of-building-automated-testing-culture-into-organization-2019-summer-edition

### 戦略

#### レガシーコードの定義

* テストコードがないもの
* 古い技術を呼ぶものではない

#### ２つのならわし

* テストを書く時間はない
  * テストを書かないから時間がなくなる
* 動くコードに触れるな
  * 触れなければ競争力が弱まり、事業が死んでいく
* Cover & Modify
* 文化を変えていく

#### イマココから始める

* ToBeではなく、AsIsとNotToBeからはじめる
* 人は自分の速度でしか成長できない
* プロジェクトもプロジェクトの速度でしか成長できない

#### TDD被験者へのアンケート

* デバッグの工数を減らす
* 要求が洗練
* コードの品質をあげる
* 開発工数を減らす

#### テストは品質を上げない

* 品質がわかるようになる
* 品質をあげるのは設計とプログラミング
  * 再設計・リファクタリングをテストで支える

### 戦術編

#### ２つの道しるべ

* レガシーコード改善ガイド
* レガシーソフトウェア改善ガイド

#### どこにテストを書いていくか

#### どこからやるか

* もっともこまっているところ
* 新機能開発
* バグ修正

#### テストのトリアージ

* リスクを見積もる
  * テストケースに対するリスクを見積もる
* 手動テストのコスト
* 自動化コスト
* 優先順位を付けて並び替え

#### どうテストを書いていくか

* レガシーコード改善の技法

#### こだわらない

* 最初から全部やらない
* テスト駆動・テストファーストにこだわらない
* ユニットテストにこだわらない

#### こだわるポイント

* 再現・繰り返し可能（Repeatable）
* 独立している（Independent）

#### 設計の可動域を確保する

* テストがないのは既に設計が悪い兆候
* 設計・実装を変えるのが前提

#### 背中をみせる

* サンプルとデモが大事
* 真似してもらう土台をつくる

-----

## C-5 アジャイル組織の作り方教えます

### 概要

* 14:15～15:00
* 片岡 俊行氏[ゆめみ]
* https://speakerdeck.com/raykataoka/aziyairuzu-zhi-falsezuo-rifang-jiao-emasu

### ３つのハマりポイント

* 階層型組織
* フラット型組織
* 権限委譲
 
### 階層型組織

* 責務の分解

### フラット型組織　

* 階層のフラット化
* コミュニケーションが一部に集中

### 権限委譲

* 入れ子構造

### 権限委譲の難しさ

* 任せる側と任せた相手に口出しをしにくくなる。
* 失敗時のプレッシャーが大きくなる
* 意見する側が権威がある場合、圧力が発生する。

### 自律・分散・協調

### ティール組織：助言プロセス

* 深く影響がある全ての関係者
* その分野の専門家

### プロポーザルとレビュー

* Slack使用

### Teamの構造

* コミッター
  * 遂行責任
  * コミット権限
  * 複数人で冗長化
* コントリビューター
  * コミット権限はない
* ダブルリンキング
  * 親チームのコミッターは子チームのコミッターになれない
  * 逆も同じ
* チームの上限を７名
* リードチームが存在

----

## A-6 ティール型組織でサービス立ち上げが成功した話

### 概要

* 15:15～15:35
* 手塚 卓也氏[スリーシェイク]

### 縦割り開発組織の問題

* 情報が不透明
* マネジメント工数肥大
* 意思決定の遅延

### ３つの失敗

* 企画の失敗
* 技術の失敗
* 組織の失敗

### ティール組織とは

* 人：ゴールに向かって自走
* 組織：互助的に自律、統治しない
* 情報：すべての情報にアクセス
* 評価：メンバーの感謝

### 企画がよくなった

* 1人企画からチーム全体で考える
* ユーザー視点が根付いた

### 技術がよくなった

* ゴールを見据えてアーキテクト設計可能に
* メンバーの技術力向上

### チームがよくなった

* 各メンバーのモチベーション向上
* 意思決定のスピードアップ

### 工夫と課題

* サポーター制度
  * 得意領域に対してサポーター認定
* 採用活動
  * チーム全員

----

## C-7 SI × Webの総合力で切り拓く新しいエンジニアのキャリアパス

### 概要

* 15:50～16:35
* 田中 清氏[メドレー]

### エンジニアを取り巻く状況の変化

* 2010年代以降、クラウドサービスなどの台頭
* エンジニア不足
* WebのテクノロジーとSI力の組み合わせスキルが必要となってきている

### SI系とWeb系の比較

* SI
  * 業務知識
  * ドキュメント
  * 堅実
* Web
  * スピード感
  * 柔軟

### X-Techの特徴

* 国が定めた制度やガイドラインを遵守したシステムとする必要
* 外部システム連携
* 必要に応じて関係省庁との関係性も重要

* AWS Config
  * ルールによる異常設定監視
  * 履歴保存、閲覧

* PMと事業部長の２トップ体制


### これからのエンジニアに求められること

* 技術を磨き進化させそれを社会に還元する
* エンジニアの本質を追求する

----

## A-8 クラウドネイティブ時代のマルチテナントアーキテクチャとデータ設計

### 概要

* 16:50～17:10
* 和田 夏帆氏[エイトレッド]

### アーキテクチャ

* バックエンド：Java（JAX-RX）
* フロントエンド：TypeScript（AngularJS）
* DB
  * MongoDB/MariaDB
  * Elasticsearch
  * Redis
* アプリケーション層はマルチテナントで共有。LB使用
* DBは機能分割
* APサーバ
  * APIおよびバッチ処理 Tomcat
  * 静的コンテンツの配信 nginx
  * AWS ECSで管理
* DBサービス
  * EC2
  * プライマリ１、レプリカ２
* Elasticsearch
  * EC2
  * 利用したい機能が無効化されていたため、AWSのサービスは使用せず
* リクエストのテナント識別方法
  * URLドメインで識別
  * セッション情報に持たせる

### パフォーマンス改善に向けた取り組み

* CloudWatch Logs Insights によるパフォーマンス分析
  * ログに出力して、クエリで抽出
* ALBを利用したパスベースルーティング  
* 資源の占有を制限。呼び出し数、レコード数、アップロード上限など

----

## A-9 あらゆるものをカイゼンせよ

### 概要

* 17:25～18:25
* 市谷 聡啓氏[ギルドワークス・エナジャイル]/新井 剛氏[ヴァル研究所・エナジャイル]/小田中 育生氏[ナビタイムジャパン]
* https://www.slideshare.net/papanda/20-153121944
* https://speakerdeck.com/araitakeshi/si-falsepurodakutohahui-she-zu-zhi-hui-she-woaziyairuzu-zhi-hua-surutamefalsezu-zhi-kai-fa-falseshi-jian
* https://www.slideshare.net/NavitimeJapan/ss-153110354

### ナビタイム

* Slackアプリができたよ
* バックログを一つ消化するごとにビジョンに近く
* 優先順位が相反する
* 優先度付けがコスト化
* カイゼンがデグレを生む
* バックログの棚卸しを定期的に実行
  * 不要・把握が困難・数ヶ月たったものをクローズ・削除する
* デグレを引き起こさない環境をつくる
  * リグレッションテスト
  * 複雑なコードとプロレスを解きほぐす
  * カイゼンデーの実施
* インセプションデッキ
* 狩野モデル
  * 当たり前品質
  * 性能品質
* USMの導入
* プロダクトはリリースされてからスタート

### ヴァル研究所

* 組織開発の必要性
  * カイゼンジャーニーにプラクティス書いてあるよ
* 価値観ババ抜きチームビルディング
* VSM作成支援
* SoE/SoRガーディアン

### ギルドワークス

* プロダクトオーナーの民主化
* アジャイル開発は２度失敗する
  * 習慣をチームで身に付けること
  * 開発チームとプロダクトオーナーの間に生まれる境界線
* プロダクトづくりの不吉なにおい
  * POが何をしていて、どうやってPBLをつくっているか開発チームが知らない。
* 開発チームからPO側への越境
  * POの役割をチームで補完する
* 現実のPOはそもそもソフトウェア開発自体がほぼ初めて
* プロダクトオーナー代行
  * 開発側はPO
  * ビジネス側ではPBLリファイメント参加
* 仮説検証型アジャイル開発
* プロダクトオーナーの民主化に向かうべき
  * PO代行は経験・スキルを補完するための便宜的な役割
  * 仮説検証の学びからプロダクトの基準をつくり、チームに宿すようにする
  * 仮説検証リードが必要

