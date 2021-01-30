# Mac初期設定  

## マシン設定  

* トラックパッド設定変更
  * システム環境設定 -> トラックパッド
    * `スクロールの方向：ナチュラル` のチェックを解除
    * `フルスクリーンアプリケーション間をスワイプ` をチェック
* 日時表記変更  
  * システム環境設定 -> 日付と時刻
    * 24時間表示、秒表示
    * 曜日を表示、日付を表示にチェック
* 電源表記変更  
  * システム環境設定 -> 省エネルギー
    * `メニューバーにバッテリーの状況を表示` をチェック
* 非表示フォルダ表示  
  * command + shift + .(ドット）
  * `defaults write com.apple.finder AppleShowAllFiles TRUE`
* 拡張子表示
  * Finder -> 環境設定 -> 詳細
    * `すべてのファイル名拡張子を表示` をチェック
* Spotlightのショートカットを無効化
  * システム環境設定 -> キーボード -> ショートカット -> Spotlight
    * `Spotlight検索を表示` のチェックを解除

* ライブ変換無効
  * システム環境設定 -> キーボード -> 入力ソース
    * `ライブ変換` を無効
    * `タイプミスを修正` を無効
* Mission Control
  * システム環境設定 -> Mission Control
    * 「最新の使用状況に基づいて操作スペースを自動的に並び替える」のチェックを外す

## 開発環境設定  

* Git  
  * 鍵情報など
* Node.js  
* VSCode
  * コンテキストメニューに追加
    * Automatorで追加
    * https://qiita.com/hiroyuki7/items/a3fcdf943c313473ecee
* Skitch
  * セキュリティとプライバシーで画面収録を可能にする
  * 環境設定、同期でEvernoteに保存を手動にする
* Postman
* HomeBrew

## Chrome

* デバッグ用の設定
  * Automator -> アプリケーションの作成 -> シェルスクリプトを実行
    * `open -a /Applications/Google\ Chrome.app/Contents/MacOS/Google\ Chrome --args  --remote-debugging-port=9222`
    * アイコンについては「情報を見る」から設定
* 拡張機能
  * [Angury](https://chrome.google.com/webstore/detail/augury/elgalmkoelokbchhkhacckoklkejnhcd) - Angularデバッグを補助してくれる拡張
  * [Redux DevTools](https://chrome.google.com/webstore/detail/redux-devtools/lmhkpmbekcpmknklioeibfkpmmfibljd?hl=ja) - NgRx使用時のデバッグ補助
  * [Linkify JIRA Issues](https://chrome.google.com/webstore/detail/linkify-jira-issues/ekbbnaokafbanjgmcbllligemhiclbcb) - WEBサイトにJIRAチケットのリンクを差し込む拡張。GitHubサイトで有効化すると良い
  * [abehiroshize](https://chrome.google.com/webstore/detail/abehiroshize/okffapkklocfabdipcgpaiibomcjdopp) - WEBサイトを爆速にする
  * [MISAWA::MD](https://chrome.google.com/webstore/detail/misawamd/legplkhbgdelfceignhcchogkmoflagl?hl=ja) - Markdownで入れる画像に悩んだ時に


