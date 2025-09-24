# Jekyll + Markdown + GTM (GA4) Starter

**Markdown で記事を書きつつ、GTM 経由で GA4 を導入**できる GitHub Pages 向けスターターです。

## 使い方（ざっくり）

1. このフォルダを GitHub の新規リポジトリへ push
2. `_config.yml` を編集：
   - `url` と `baseurl` を自分の公開 URL に合わせる
   - `gtm_container_id: "GTM-XXXXXXX"` を自分の **GTM ID** に置換
3. GitHub → Settings → Pages → Source を `GitHub Actions`（推奨）に
4. 初回ビルド後、公開 URL にアクセス（`https://username.github.io/repo/`）

## ローカルで試す（任意）

```bash
gem install bundler
bundle install
bundle exec jekyll serve
# http://127.0.0.1:4000/<your-repo>
```

## 記事の追加

`_posts/YYYY-MM-DD-title.md` を作成して Markdown を書くだけ。

## GA4 の設定（GTM 経由）

- GTM で Web コンテナ作成 → `GTM-XXXXXXX`
- GTM で **GA4 設定タグ** を作成し、トリガを「All Pages」に
- クリック計測などは GA4 イベントタグ + トリガ（例：カスタムイベント `cta_click`）で

## 注意

- GitHub Pages の Jekyll バージョンに合わせるため、`github-pages` gem を使用しています。
