# Developers Summit 2018 Summer

## 概要

* 日時：2018年7月27日(金) 10:00-17:45
* URL：https://event.shoeisha.jp/devsumi/20180727

## ブログ記事

* https://kakkoyakakko2.hatenablog.com/entry/2018/07/28/130000

## A-3: とあるマーケティング部隊とデータエンジニアのデータドリブンへの道

* モンスト
* データ分析の問題
  * 仕様書
  * コードを読む
  * 複雑なテーブル
  * 長すぎるSQL
  * サマリーテーブルの乱立
* BIツールは助けてくれない
* Dimensional Modeling
  * Data Warehouseの要件に合わせたテーブル設計
  * Star Schema
    * DIMENSIONS:Factに対する説明
    * FACT:イベント状態
  * 設計の手順
    * ビジネスプロセスを選ぶ
    * 粒度
    * Dimensionテーブルを決める
    * Factテーブルを決める
  * メリット
    * クエリのパフォーマンス
    * 分析軸を柔軟に追加
    * データを理解しやすい
* 作戦
  * 重要なビジネスプロセスから順番に着手
    * ビジネスプロセスの分析・粒度をちゃんときめておくとDWH全体の生合成を保てる
* つらかったこと
  * 設計コスト：設計に時間がかかる
  * Hive, Redshiftでは難しい部分も：データ更新・実行効率

---

## B-4: 教えて!goo  

### 1.gooのAIの目指すもの

* gooのAIの進化  
  * 共感、理解
  * キャラクター性
  * 対話
  * おもてなし
* 人に寄り添うAIを通じ、人の創造的な活動支援
  * 気づき、予想外

### 2.恋愛相談AIオシエル

* QAコミュニティ上で恋愛相談に長文で回答
* 回答の評価から再学習
* 教えてgooの課題
  * 即時性
  * 回答率
  * 満足度
* 3000万件の集合知
* 回答の構成
  * 共感
  * 結論
  * 理由
  * 励まし
  * 名言
* good:17%, ベストアンサー:5%
* NNAモデル
  * Non-Factoid:答えが多様・複雑・長文
* QA-LSTM
  * Word2vecで単語ベクトル生成
  * Bi-LSTMによる文書ベクトル生成
  * 類似度計測でマッチング最適化　
* NTTレゾナント手法　
* 提案手法によるQAシステム  
  * 単語ベクトル学習
  * 回答生成学習
* Make Attention

### 3.チャットボット版AIオシエル

* docomoのmydaiz上に登場
* 数ターンのセッションで回答
* 耳をすませばのケースでデモ
* パーソンライズの効果：ユーザの相談文脈にそった、ハズレ感のない応答
* パーソナライズLSTM - PLSTM
* 過去の発話の現在の発話応答への重みを学習

### 4.対話AIの未来

* 文字レベルでの長文自動生成に現在取り組んでいる
* Seq2seq
* Neural Answer Generation Model
* GPU 20GB
* 計算時間：約１週間

---

## A-5: Alibaba Cloud

### 1.Alibaba Cloudについて

* 中国でのシェアバイク・監視カメラ等でクラウド環境として利用されている
* ECサイト等の自社サービスをOne IDで管理している基盤で利用
* 日本サイトでは一部のプロダクトのみ利用できる

### 2.Alibaba Cloudの基盤技術

* 分散処理を支えるプラットフォーム
* 分散ファイルシステム
  * Block Storage
  * Object Storage
  * Table Store
  * Bigdat Service
  * Message Queue
* リリースジョブスケジューラ
  * Master-Agent構成
  * スケールのしやすい設計
  * リリーススコアリングを定期的に収集、スコアリングに応じて障害判定
* Hiveより３倍程度早い

### 3.最近のAlibaba Cloudプロダクト情報 

* Container　Service: Docker/Kubernetes対応
  * Serverless Kubernets(Closed β)：クラスタの運用不要
* IoT Platform
  * SDK
  * IoT Hub
  * デバイス管理
  * 連携プロダクト

---

## A-6: Rakuten Rapid API  

### 楽天とAPI

* API戦略
  * Step1:Private API
  * Step2:Public API (2006-)  
  * Step3:API marketplace (2018-)
* Private API 
  * Shopping/Ichiba/会員情報API <- API Gateway -> Service
  * 120億リクエスト/月
* Public API
  * 楽びん

### Rakuten Rapid API

* APIマーケットプレイス
  * APIプロバイダ
  * APIを利用する開発者
* APIプロバイダ
  * 探索
  * 収益化
  * コミュニティ
  * 管理
* アプリ開発者
  * 探索
  * 利用
  * 管理
  * 支払い
* 8000を超えるAPIを提供
* 日本語サポート・管理ページはほぼ日本語
* ダッシュボードで複数のAPIを管理できる
* vue.js + VSCodeでデモ
* 開発者サイトでAPIキー発行するAPIとRapid APIサイト内で発行するAPIがある。(提携状況によりかわる)
* MSのAPIとは提携

---

## C-7: Clova Extensions Kitで創る新しいUXと社会 

### LINEプラットフォーム戦略

* メッセンジャー
* 広告
* FinTech
* AI 

### AIアシスタントClova

* AI = Virtual Assistant in our life
* Architecture  
  * Client
  * Brain
  * SKill
* Natural language understanding
  * Word segment, tagging (形態素解析)
    * NEologd -> MeCabに辞書追加
  * Sentence Similarity
    * Resembla
  * Model manager: Drucker

### CEK (Clova Extension Kit)

### Clovaスキルで実現できる世界

* スキル
  * 天気・ニュースの検索
  * TODOリスト
  * 遅延情報
* Bot
  * 結果をLINEアカウントへ送信
* 手を使えないケース
* 他機器との連携

### CEKの使い方

* VUI
  * 入力パターンが様々。定型ではない。
* CodeZineで連載あり


---

## A-8: 1日10TB以上の店舗映像を解析するサービスの仕組みとノウハウ 

### ABEJA Platform

* AI Platform
* データ取得・機械学習を総合的にサポートするプラットフォーム
* 店舗向け・製造業向けのパッケージもあり

### ABEJA Insight for Retailの仕組み

* 店舗内カメラの映像解析
  * 人のカウント
  * 年齢
  * 性別
  * リピーター推定機能
  * 導線分析サービス

### サービス拡大時に困ったこと

* サービスの阻害要因
  * IoT
    * デバイス導入コスト
    * デバイス故障対応
      * 初期不良
      * 群発故障：物理破損、電源、ネットワーク、ファームウェア
      * 寿命による故障
  * AI
    * 多様化するデバイス・アルゴリズムの対応
    * 大量のパラメータ管理：デイバイス関連パラメータ、AI関連パラメータ

### サービス拡大の取り組み

* デバイスの安定性改善
* 拡張・スケール可能
* チームでサービス導入・運用できる体制構築
  * 徹底的なツール開発
    * ツールがないと属人化、大量の仕事がさばけない
  * プロセスの継続的な改善

