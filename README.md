# アンソロウ Marketplace

> **稼働版**: v1.7（2026年5月5日）パスワードレス認証付きマーケットプレイスPWA
> **配色**: 旧紙 #f5ecde / コーラル #d97757 / セリフ見出し（Anthropic Claude準拠）

## 公開URL

**https://haruki129.github.io/anthrou-app/** （GitHub Pages 稼働中）

iPhone Safari で開いて「ホーム画面に追加」するとPWAとしてネイティブアプリ並みに使えます（オフライン閲覧対応）。

## 最初に開くファイル

**[current/index.html](current/index.html)** — 統合マーケットプレイス本体（v1.7・162KB / 1725行）

## 機能サマリー

- **パスワードレス認証** — メール+6桁OTPコード（リアルタイム検証・タイポ提案・自動ログイン）
- **トーク** — チャット（送受信・添付・typing・ダミー返信）+ マッチング詳細+応募
- **検索** — 4チップフィルター（すべて/スキル/完成/未完成）+ 新規公開モーダル（写真動画+価格3モード）
- **状態** — 4セクション（取引/利用/問合せ/収益）+ 詳細画面7種
- **保存** — 3セグメント（お気入り/DL/履歴）+ 各詳細遷移
- **設定** — プロフィール編集・アカウント情報・ログアウト
- **PWA** — manifest + ServiceWorker（ホーム画面追加・オフライン閲覧対応）

## ディレクトリ構成

```
アンソロウ デザイン/
├── README.md                  ← 本ファイル
├── index.html                 ← ルート（current/index.html へリダイレクト）
├── current/                   ← 現行版 v1.7 稼働中
│   ├── index.html             ← マーケットプレイス本体
│   ├── manifest.webmanifest   ← PWA定義
│   ├── sw.js                  ← ServiceWorker
│   └── assets/                ← ロゴ画像7種
└── versions/                  ← 3版リテンション（v1.5 / v1.6 / v1.7）
```

## バージョン履歴ハイライト

- v1.7 — パスワードレス認証（OTP+localStorage自動ログイン）
- v1.6 — 保存タブ詳細（お気入り/DL/履歴）
- v1.5 — 詳細画面7種+収益状況追加
- v1.4 — 状態タブ刷新（取引/利用/問合せ）
- v1.3 — チャット/プロフィール/マッチング 稼働化
- v1.2 — ロゴ背景 旧紙化
- v1.0–v1.1 — ロゴ統一（コーラル「ハウス+ルーフ」）
- v0.7 — 検索フィルター刷新（スキル/完成/未完成）
- v0.6 — PWA化
- v0.5 — Anthrou Marketplace 単一HTML再構築

## ローカル起動

```bash
cd アンソロウ\ デザイン
python3 -m http.server 8080
# ブラウザで http://localhost:8080/ を開く
```

ServiceWorker は `file://` プロトコルでは動かないため、HTTPサーバ経由必須。

## ライセンス

© 2026 樋口 — All rights reserved.
