# 仮想中央競馬データベース — GitHub Pages公開用 (Ver.41)

## 公開方法

1. GitHubで新しい**Public**リポジトリ（例: `kachu-racing`）を作成します。
2. このZIPを解凍し、`index.html`、`.nojekyll`、`README.md` をリポジトリの**ルート**にアップロードし、コミットします。（ZIPファイルそのものをアップロードするのではありません）
3. リポジトリの **Settings → Pages** で **Build and deployment → Source: Deploy from a branch** を選び、`main` と `/(root)` を選択して **Save** します。
4. 公開先は一般に `https://<GitHubユーザー名>.github.io/<リポジトリ名>/` です。リポジトリの Pages 設定画面の **Visit site** から確認してください。

## 保存データについて【重要】

このVer.41はブラウザの `localStorage` を使用します。同一URLでも、**ブラウザ・端末ごとに別々のデータ**が保存されます。GitHubに公開するだけで、閲覧者全員が同じレースデータを見られるわけではありません。

- サイト公開用ZIPには競馬データのJSONバックアップを**同梱していません**。元のVer.41などでJSONバックアップを作り、公開サイトの「バックアップ復元」から読み込めば、**そのブラウザだけ**にデータを取り込めます。
- 公開リポジトリに個人情報・非公開戦績・バックアップJSON・APIキーなどをアップロードしないでください。
- サイトのURLが変わるとブラウザの保存領域も変わります。必ずJSONバックアップを保持してください。
- OCRは外部のTesseract.js CDNを利用するため、利用時にインターネット接続が必要です。
- 全員が閲覧できる共通データベースを実現したい場合は、公開用JSON/API（読み取り専用）などの連携実装が別途必要です。

## 更新

更新時には`index.html`を新しいバージョンのHTMLに置き換えてコミットしてください。ブラウザの保存データは変えずにアプリを更新できる可能性がありますが、重大な更新の前にはJSONをエクスポートして保管してください。

## 参照

https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site
