# 幻獣物語2 挟み変化用ルート検索ツール

GitHub Pages で動作する静的サイト版です。Google Apps Script (`google.script.run`) への依存を取り除き、同梱 JSON を `fetch()` で読み込みます。

## ファイル構成

- `index.html` — 検索画面・検索処理
- `data/幻獣図鑑.json` — 幻獣図鑑データ
- `data/変化ルート.json` — 変化ルートデータ

## GitHub Pages で公開

1. GitHub でリポジトリを作成します。
2. この ZIP の中身をリポジトリのルートにアップロードします。`index.html` と `data/` が同じ階層になるようにしてください。
3. リポジトリの **Settings → Pages** を開きます。
4. **Deploy from a branch** を選び、`main` と `/(root)` を指定して保存します。
5. Pages に表示された URL を開きます。

`index.html` をファイルアプリ等から直接開くと、ブラウザーの制約で JSON 読み込みが失敗することがあります。GitHub Pages またはローカル HTTP サーバー経由で開いてください。

## 注意

- ルート JSON は約 40 MB あります。初回読み込みに時間と通信量がかかります。
- 数値列は元データの5項目を S / A / D / A+D / S+A+D として扱っています。
- ブラウザーでの実機・表示確認は未実施です。データ構造と JavaScript の構文は確認しています。
