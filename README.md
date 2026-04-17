# fudebako

ブラウザ内で動作する Python データ解析ツール。インストール不要、インターネット接続不要。お客様のデータはすべてブラウザ内で処理され、外部に送信されることはありません。

## 特長

- **ローカル完結** — 起動後はネットワーク通信なし。外部通信が制限された環境でも使用可能
- **インストール不要** — 単一の HTML ファイルをダブルクリックするだけで起動
- **Python 搭載** — WebAssembly 上の Python 3.13 により、データ前処理・統計処理・可視化をブラウザ内で完結
- **グラフ描画** — matplotlib による静的プロット、ズーム・パン・画像保存に対応
- **永続ストレージ** — ブラウザ内に `/drive/` 領域を保持。作業途中の CSV やスクリプトを保存し、次回起動時に再開可能

## ダウンロード

[Releases ページ](https://github.com/yonaka15/fudebako/releases/latest) から最新版の `fudebako-vX.Y.Z.html` を取得してください。

## 動作要件

| 項目 | 要件 |
|------|------|
| ブラウザ | Google Chrome / Microsoft Edge / Mozilla Firefox 最新版 |
| メモリ | 2 GB 以上推奨 |
| ファイルサイズ | 約 40 MB |
| ネットワーク | 起動時・実行時ともに不要 |

## 使い方

1. ダウンロードした HTML ファイルをダブルクリックし、既定のブラウザで開きます
2. 初回起動時は Python ランタイムの初期化に 20〜30 秒かかります。完了後「準備完了」と表示されます
3. 左側のエディタに Python コードを入力し、`Ctrl + Enter` (macOS: `⌘ + Enter`) で実行します

## ライセンス

- [**TERMS.md**](TERMS.md) — 利用規約 (日本語、正本)
- [**LICENSE**](LICENSE) — 英語参考訳 (齟齬がある場合は TERMS.md が優先)
- [**docs/THIRD_PARTY_LICENSES.md**](docs/THIRD_PARTY_LICENSES.md) — 同梱される第三者コンポーネントの一覧
- **NOTICES.txt** — 各 Release に添付。第三者ライセンスの全文を収録

本ソフトウェアは「現状有姿 (AS IS)」で提供されます。詳細は [TERMS.md](TERMS.md) をご確認ください。

## お問い合わせ

- 不具合報告・機能要望: [Issues](https://github.com/yonaka15/fudebako/issues)
- 脆弱性報告: [SECURITY.md](SECURITY.md) を参照

---

Copyright © 2026 yonaka15. All rights reserved.
