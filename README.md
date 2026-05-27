# nocame-legal

iOS アプリ「NoCame (ノーカメ)」のプライバシーポリシーおよび利用規約 (EULA) を配信するための静的サイトです。GitHub Pages で公開し、App Store Connect の「プライバシーポリシー URL」「利用規約 URL (EULA)」に登録します。

## 構成

| ファイル | 内容 | 公開後の URL (例) |
| --- | --- | --- |
| `index.html` | トップページ。両ページへのリンク + アプリ簡易説明 | `https://<user>.github.io/nocame-legal/` |
| `privacy.html` | プライバシーポリシー | `https://<user>.github.io/nocame-legal/privacy.html` |
| `terms.html` | 利用規約 (EULA) | `https://<user>.github.io/nocame-legal/terms.html` |
| `README.md` | このファイル | — |

## GitHub Pages 有効化手順

1. GitHub にログインし、新規リポジトリ `nocame-legal` を作成 (Public)。
2. ローカルでリポジトリを初期化し、本ディレクトリの内容をプッシュ。

   ```bash
   cd /Users/nakano/nocame-legal
   git init
   git add .
   git commit -m "Initial commit: NoCame privacy policy and terms of use"
   git branch -M main
   git remote add origin git@github.com:<your-username>/nocame-legal.git
   git push -u origin main
   ```

3. GitHub のリポジトリページで **Settings → Pages** を開く。
4. **Build and deployment** セクションで以下を設定。
   - Source: `Deploy from a branch`
   - Branch: `main` / `/ (root)`
   - **Save** をクリック。
5. 数十秒〜数分待つと、Pages のページ上部に公開 URL が表示される。
   - 例: `https://<your-username>.github.io/nocame-legal/`
6. ブラウザでアクセスし、`index.html`・`privacy.html`・`terms.html` が表示されることを確認。

## App Store Connect への登録

App Store Connect の以下の項目に URL を登録します。

- **App Information → Privacy Policy URL**: `https://<your-username>.github.io/nocame-legal/privacy.html`
- **App Information → License Agreement** (任意の EULA を使う場合): `https://<your-username>.github.io/nocame-legal/terms.html`
- **Subscription Group → Review Information** にも EULA URL を貼ると審査がスムーズです。

## カスタムドメインを使う場合 (任意)

`nocame.example.com` のような独自ドメインを使う場合は、リポジトリ直下に `CNAME` ファイル (中身はドメイン名のみ) を置き、DNS の CNAME レコードを `<your-username>.github.io` に向ければ Pages 側で SSL が自動発行されます。

## 内容の更新について

- ポリシーや規約を改定する際は、各 HTML ファイル冒頭の「最終更新日」を必ず更新してください。
- 重要な変更がある場合はアプリ内通知や App Store の更新説明にも記載することを推奨します。

## 連絡先

- 開発者: 中野遥 (haru nakano)
- メール: nakanoh082986@gmail.com
