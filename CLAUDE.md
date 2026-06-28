# CLAUDE.md

このリポジトリは Hugo 製の個人ブログ（`punchdrunker.tokyo`）です。

## 基本情報

- 静的サイトジェネレータ: **Hugo**（extended, v0.152 系で動作確認）
- テーマ: **paper**（`themes/paper` は git submodule）
- 記事の置き場所: `content/post/`
- 画像など静的ファイル: `static/`（サイトのルート `/` に配置される）
- ビルド成果物: `public/`（**Git管理対象。コミットに含める**）
- 公開: **GitHub Pages が `main` ブランチを配信**（CI/CD なし。手動ビルド＆コミット運用）

## 記事を書く

`content/post/YYYY-MM-DD.md` を作成。front matter の例:

```markdown
---
title: "タイトル"
date: 2026-06-28T10:52:00+09:00
draft: false
images: ["/cornixlp.jpg"]   # SNSシェア用サムネイル(OGP)。任意
cover: "/cornixlp.jpg"       # 同上。任意
tags: ["report"]
---
```

## 画像

1. 画像を `static/` に置く（例: `static/foo.jpg`）
2. 本文から **先頭スラッシュ** で参照する（`static/` は付けない）:
   ```markdown
   ![説明テキスト](/foo.jpg)
   ```
3. サムネイル（SNSシェア時の画像）にしたい場合は front matter に `images` / `cover` を追加。
   - これは **ページ上には表示されない**。`<head>` の `og:image` / `twitter:image` として出力される。
   - **本番ビルド時のみ**出力される（`hugo server`（開発モード）では出ないので注意）。
   - 確認: `hugo` でビルド後 `grep og:image public/post/<記事>/index.html`
4. 画像は重いとSNS表示や速度に影響するので、横1200〜1600px・数百KB程度にリサイズ推奨。
   - 例: `sips -Z 1600 static/foo.jpg`（macOS）

## ローカルプレビュー

```bash
hugo server -D   # -D で draft も表示。http://localhost:1313/
```

## 公開（デプロイ）手順

CIが無いため **`public/` をビルドしてコミットに含めて push** する。

```bash
hugo                                  # public/ を本番ビルド（環境はデフォルトで production）
git add content static public         # ※ themes/paper(submodule)の差分は含めない
git commit -m "new post: <タイトル>"
git push origin main                  # GitHub Pages は main を配信
```

注意点:
- **`hugo` のビルドを忘れると `public/` が古いまま公開される。** 記事を直したら必ず再ビルド。
- 公開対象ブランチは **`main`**（リポジトリの default branch は master だが、Pages は main）。
- `themes/paper` は submodule。記事更新では基本コミットに含めない（`git add -A` ではなく `git add content static public` を使う）。
- 反映には GitHub Pages のビルド/CDNで数分のタイムラグがある。
- 公開後の見た目確認: https://punchdrunker.tokyo/post/<YYYY-MM-DD>/
