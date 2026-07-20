# 臨床試験規制情報Wiki: LLM Wiki

Mode: E (Research) — 規制文書特化型
Purpose: 臨床試験に関連する規制要件・ガイドライン・ガイダンス・Tips情報の集積と分類
Owner: renyuhki
Created: 2026-04-22

## Structure

```
vault/
├── .raw/              # 原典PDF、ウェブクリップ、ガイドライン原文
├── wiki/
│   ├── index.md       # マスターカタログ
│   ├── log.md         # 操作ログ（追記のみ）
│   ├── hot.md         # ホットキャッシュ（直近コンテキスト ~500語）
│   ├── overview.md    # Wiki全体サマリー
│   ├── guidelines/    # ガイドライン・ガイダンス文書サマリー（ICH/FDA/EMA/PMDA）
│   ├── concepts/      # 規制概念・用語・フレームワーク（GCP、エンドポイント等）
│   ├── entities/      # 規制機関・委員会・組織
│   ├── domains/       # 規制領域別（安全性・有効性・統計・申請等）
│   ├── comparisons/   # 規制機関間の横断比較
│   ├── questions/     # 未解決の規制上の疑問・解釈問題
│   └── meta/          # ダッシュボード、lintレポート
├── _templates/        # ノートタイプ別テンプレート
└── .obsidian/
    └── snippets/vault-colors.css
```

## Conventions

- 全ノートはYAMLフロントマターを使用: type, status, created, updated, tags（最低限）
- ウィキリンクは [[Note Name]] 形式: ファイル名はVault内ユニーク、パス不要
- .raw/ は原典文書: 絶対に編集しない
- wiki/index.md はマスターカタログ: ingest毎に更新
- wiki/log.md は追記のみ: 過去エントリは編集しない、新エントリは先頭に追加
- wiki/hot.md は毎セッション末に上書き更新

## Operations

- Ingest: .raw/ にソース配置 → "ingest [ファイル名]" と指示
- Query: 質問をそのまま入力 → ClaudeがIndexから順に読み込んで回答
- Lint: "lint the wiki" → ヘルスチェック実行
- Save: "save this" または "/save" → 現在の会話・回答をWikiに保存

## Regulatory Scope

主なカバー領域:
- ICH ガイドライン（E/S/Q/Mシリーズ）
- FDA ガイダンス文書
- EMA ガイドライン
- PMDA 関連通知・ガイドライン
- GCP / GLP / GMP
- 安全性報告（SAE、SUSAR、DSUR、PBRER）
- 臨床試験デザイン（エンドポイント、サンプルサイズ、適応デザイン）
- 統計的考慮事項
- 申請プロセス（IND/NDA/BLA/CTA/J-NDA）

## Wiki Knowledge Base

Path: D:/Apps/LLM-Wiki/llm-wiki

他プロジェクトからこのWikiを参照する際:
1. wiki/hot.md を最初に読む（直近コンテキスト、~500語）
2. 不十分なら wiki/index.md を読む（全カタログ）
3. 特定領域が必要なら wiki/<domain>/_index.md を読む
4. その後に個別Wikiページを読む
