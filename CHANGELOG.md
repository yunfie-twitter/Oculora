# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [1.1.0] - 2025-11-27

### Fixed
- **TSセグメントプロキシの修正** (#1)
  - m3u8ファイル内のTSセグメントURLが正しくプロキシ経由になるように修正
  - 相対URLと絶宮URLの両方を適切に処理
  - 空行の適切なハンドリング

### Added
- **ログの改善**
  - `[PROXY]` プレフィックスでプロキシリクエストを識別しやすく
  - m3u8ファイルのキャッシュヒット/ミスのログ出力
  - TSセグメントストリーミング開始のログ

### Improved
- **エラーハンドリング**
  - セグメント取得時のエラーハンドリングを強化
  - エラー時のスタックトレース出力を追加

- **m3u8検出**
  - `/manifest/` を含むURLもm3u8として検出

## [1.0.0] - 2025-11-XX

### Added
- 初回リリース
- YouTube動画/プレイリスト情報のREST API提供
- HLS (.m3u8)ストリーム/TSセグメントのプロキシ
- 関連動画・検索・チャンネルメタ情報取得
- コメント抽出（Selenium＋Stealthで突破）
- キャッシュによる高速化
- .env＆config.py経由で環境変数による柔軟設定

---

## アップグレード方法

### v1.0.0 → v1.1.0

1. 最新コードをpull:
```bash
git pull origin main
```

2. サーバーを再起動:
```bash
python run.py
```

追加の依存パッケージはありません。

---

## バグ報告・機能リクエスト

バグ報告や機能リクエストは [GitHub Issues](https://github.com/yunfie-twitter/Oculora/issues) までお願いします。
