# IRONHOUR（ポートフォリオ用・架空サイト）

Astro製の1ページLP。デザインはFigma「NORD-SAUNA-Top-Page」の IRONHOUR PC / Tablet / SP。

## 動かし方

```bash
npm install
npm run dev      # http://localhost:4321 でプレビュー
npm run build    # dist/ に静的ファイルを書き出し
```

Node.js 18.20.8 以上（推奨は 22 系）。

## フォルダ構成

```
src/
├── data/site.ts          … 文言（ここを直せば全体に反映）
├── styles/global.css     … 色・余白・レスポンシブ（PC / ≤1023px / ≤599px）
├── layouts/BaseLayout.astro
├── pages/index.astro     … セクションの並び順
└── components/           … セクションごとのコンポーネント
public/images/            … TOP画像（PC / Tablet / SP）
```

## 写真の差し替え

`Photo.astro` がプレースホルダーです。写真が用意できたら `public/images/` に置いて、
該当箇所の `<Photo ... />` を `<img src="/images/xxx.jpg" alt="..." />` に置き換えてください。

## 公開（Vercel の場合）

1. GitHub にリポジトリを作って push
2. Vercel で「Add New → Project」からリポジトリを選ぶ
3. Framework は Astro が自動選択されるので、そのまま Deploy
