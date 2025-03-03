[English](README.md) | 日本語

# astro-notion-blog

[![GitHub stars](https://img.shields.io/github/stars/otoyo/astro-notion-blog)](https://github.com/otoyo/astro-notion-blog/stargazers)
[![GitHub license](https://img.shields.io/github/license/otoyo/astro-notion-blog)](https://github.com/otoyo/astro-notion-blog/blob/main/LICENSE)

<img src="https://user-images.githubusercontent.com/1063435/213838069-c9654c32-ec9b-4e82-a3b5-2acbd665b16a.png" width="480">

astro-notion-blog を使えば [Notion](https://www.notion.so) で書けるブログを作ることができます。  
ブログは [Astro](https://astro.build/) を使って静的生成されるので非常に高速です。

- :rocket: ページの表示が**爆速**
- :pencil: **Notion で**ブログが書ける
- :hammer_and_wrench: ブログの見た目を**自由にカスタマイズ可能**
- :white_check_mark: **Notion 公式 API**を使っているため安心

## スクリーンショット

<img src="https://user-images.githubusercontent.com/1063435/223610351-58d157cc-fe50-4ff3-be0c-5373bec07589.png" width="600">

## デモ

[https://astro-notion-blog.pages.dev](https://astro-notion-blog.pages.dev)

## クイックスタート

### 必要なもの

- [Notion](https://www.notion.so/)
- [Cloudflare Pages](https://pages.cloudflare.com/)

### ステップ

1. このリポジトリを**スターします** :wink:
   - スターしていただけると開発の励みになります
2. [ブログテンプレート](https://otoyo.notion.site/e2c5fa2e8660452988d6137ba57fd974?v=abe305cd8b3d467285e91a2a85f4d8de) を自分の Notion へ複製します
3. 複製したページ(データベース)のアイコン、タイトル、説明を変更します

<img src="https://user-images.githubusercontent.com/1063435/223611473-09e87aba-ad3b-4380-a74f-58c3c5804c39.png" width="600">

4. 複製したページ(データベース)の URL `https://notion.so/your-account/<ここ>?v=xxxx` を `DATABASE_ID` としてメモします

<img src="https://user-images.githubusercontent.com/1063435/213966685-3a2afed2-45c0-4ea5-8070-e634d8d648de.png" width="260">

<img src="https://user-images.githubusercontent.com/1063435/213966934-4442ce75-f88e-465f-b4f4-545d46b8eec9.png" width="600">

5. [Create an integration](https://developers.notion.com/docs/create-a-notion-integration#step-1-create-an-integration) からインテグレーションを作成し "Internal Integration Token" を `NOTION_API_SECRET` としてメモします
6. 複製したページを再度開き [Share a database with your integration](https://developers.notion.com/docs/create-a-notion-integration#step-2-share-a-database-with-your-integration) の手順でインテグレーションにデータベースを共有します
7. このリポジトリを自分のアカウントヘフォークします
   - フォークボタンは画面上部右側のスターの左にあります
8. [Cloudflare Pages](https://pages.cloudflare.com/) を開きサインインします
   - 言語設定を日本語に変更します

<img src="https://user-images.githubusercontent.com/1063435/213967607-338b8728-d7c9-47e4-8192-e955e3f4ce30.png" width="220">

9. プロジェクトを "Connect to Git" を選んで作成し、先ほどフォークした `<your-account>/astro-notion-blog` リポジトリを選んで "Begin setup" をクリックします
10. 「ビルドの設定」で、
11. 「フレームワーク プリセット」で Astro を選択します
12. 「環境変数(アドバンスド)」 を開き `NODE_VERSION`, `NOTION_API_SECRET`, `DATABASE_ID` の 3 つを設定します
    - `NODE_VERSION` は `v16.13.0` かそれ以上を指定します
    - 詳しくは [How to deploy a site with Git](https://docs.astro.build/en/guides/deploy/cloudflare/#how-to-deploy-a-site-with-git) をご覧ください

<img src="https://user-images.githubusercontent.com/1063435/213967111-72ea2ad1-ad3b-4629-8b65-7b25bc6ddb31.png" width="400">

<img src="https://user-images.githubusercontent.com/1063435/213967331-a1de0810-a8b4-4fae-adba-110f3f4400cc.png" width="600">

11. "Save and Deploy" をクリックし、デプロイが完了すると Notion Blog が見えるようになります

astro-notion-blog では新しい記事や変更を公開したいとき毎回デプロイが必要になります。  
Cloudflare Pages のダッシュボードから手動でデプロイするか、GitHub Action のような CI を使って定時デプロイしてください。

## カスタマイズするには

### 追加の必要要件

- Node.js v16 かそれ以上
- Git
- [Yarn](https://yarnpkg.com/getting-started)

### ステップ

1. プロジェクトルートに `.env` ファイルを作成し下記のように環境変数を書き込みます

```sh
NOTION_API_SECRET=<YOUR_NOTION_API_SECRET>
DATABASE_ID=<YOUR_DATABASE_ID>
```

2. 依存関係をインストールしローカルサーバーを起動します

```sh
yarn install
yarn dev
```

3. ブラウザで [http://localhost:3000](http://localhost:3000) を開きます
4. 開発サーバーを停止するにはターミナルで `Ctrl+C` を押します。

### その他の情報

[wiki](https://github.com/otoyo/astro-notion-blog/wiki) をご覧ください。

## バグ報告 & 機能要望

Issue を作成してください。日本語で大丈夫です。

## :bird: Twitter コミュニティ

コミュニティに参加して他のメンバーからサポートを受けたりサポートすることができます。

- [astro-notion-blog](https://twitter.com/i/communities/1618017732653613056)

## 貢献

Pull requests 歓迎です。

---

astro-notion-blog は [otoyo/notion-blog](https://github.com/otoyo/notion-blog) をベースにしています。
