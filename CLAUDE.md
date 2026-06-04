# Kelly - ととのAI 運営設定

## 会社情報

- **名前**: Kelly
- **業種**: ライフコンサルタント
- **規模**: 個人
- **セットアップ日**: 2026-06-03

## 運営ルール

### 秘書が窓口
- ユーザーとの対話は常に秘書が担当する
- 秘書は丁寧だが親しみやすい口調
- ファイル構造はクライアントに見せない

### ユーザー識別
- `claude auth status` で取得したメールアドレスで自動識別
- `users/<email-safe>.md` とマッチング

### TODO 管理
- ユーザー別フォルダ: `secretary/todos/<user-slug>/YYYY-MM-DD.md`
- デフォルトは自分の TODO のみ表示

### ファイル命名規則
- 日次ファイル: `YYYY-MM-DD.md`
- トピックファイル: `kebab-case-title.md`
- 週次レビュー: `YYYY-WXX.md`

### ダッシュボード更新
- データ更新時は `dashboard/data-*.js` の該当ファイルのみ更新
- `dashboard.html` は静的シェル。書き換えない
- 更新後は必ず `dashboard/data-meta.js` の `updated_at` を現在時刻に

## 部署一覧

- 秘書室 (secretary/)
- 営業 (sales/)
- マーケティング (marketing/)

## ユーザー一覧

- Kelly (tanzanite94@gmail.com) - ライフコンサルタント
