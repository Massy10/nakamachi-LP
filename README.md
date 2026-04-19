# ナカマチ LP — AI × 個人開発

非エンジニアが、AIでプロダクトをつくる。ナカマチの活動紹介ランディングページ。

## 特徴

- **Seedance 2.0 動画背景** — ○○君キャラクターのAI生成アニメーションがスクロールと連動
- **リキッドグラスUI** — 全カード・ナビに統一されたグラスモーフィズム
- **スクロール連動** — `video.currentTime` をスクロール位置にリアルタイム同期
- **ダークセクション自動切替** — Services/CTAセクションで背景オーバーレイが自動暗転
- **モバイルファースト** — X経由スマホ流入を想定したレスポンシブ設計

## ファイル構成

```
index.html                              # メインLP（単一HTML、外部依存なし）
seedance2_Video_20260419_011949.mp4     # Seedance 2.0 生成背景動画
keikakukun.png                          # 計画君キャラクター
Gemini_Generated_Image_ye2m13...png     # ワリカン君キャラクター
Gemini_Generated_Image_sqgpna...png     # 計算君キャラクター
Gemini_Generated_Image_21mg8f...png     # 調整君キャラクター
```

## ローカルで確認

```bash
# ファイルをすべて同じフォルダに置いてブラウザで開く
open index.html
```

## デプロイ

Vercel / Cloudflare Pages / Netlify にそのままデプロイ可能。

```bash
# Vercel の場合
npx vercel --prod
```

### 本番時の動画ホスティング

読み込み速度改善のため、動画は外部（Mux / Cloudflare Stream / S3）にアップロードし、
`index.html` 内の `<video src="...">` をURLに差し替えることを推奨。

## 技術スタック

- HTML / CSS / Vanilla JS（フレームワーク不使用）
- Google Fonts: Noto Sans JP, DM Sans, JetBrains Mono
- Seedance 2.0 (ByteDance) で動画生成

## ライセンス

© 2026 ナカマチ. All rights reserved.
