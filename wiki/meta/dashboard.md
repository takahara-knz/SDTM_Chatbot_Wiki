---
type: meta
title: "Dashboard"
updated: 2026-04-22
tags: [meta, dashboard]
---

# Wiki Dashboard — 臨床試験規制情報Wiki

## 最近の活動
```dataview
TABLE type, status, updated FROM "wiki" SORT updated DESC LIMIT 15
```

## Seedページ（要発展）
```dataview
LIST FROM "wiki" WHERE status = "seed" SORT updated ASC
```

## ガイドライン一覧
```dataview
TABLE issuer, series, status, effective_date FROM "wiki/guidelines" SORT issuer ASC
```

## 出典未設定のエンティティ
```dataview
LIST FROM "wiki/entities" WHERE !sources OR length(sources) = 0
```

## 未解決の疑問
```dataview
LIST FROM "wiki/questions" WHERE status = "open" SORT priority ASC
```

## 比較ページ
```dataview
TABLE topic, agencies, status FROM "wiki/comparisons" SORT updated DESC
```
