# javascript: URIスキーム テストページ

URLBlocklist で `javascript:*` を設定した際の動作検証用サンプルです。

## 用途

- Chrome管理コンソールやMDMでURLBlocklistを設定後、実際にブロックされるか確認
- `javascript:` URIと `onclick` 属性の違いを理解するための教材

## テストパターン

| パターン | URLBlocklistでブロック |
|---------|:---:|
| `href="javascript:..."` | ✅ |
| `href="#" onclick="..."` | ❌ |
| `<button onclick="...">` | ❌ |
| `<script>` タグ内 | ❌ |

## 使い方

1. フィルタリング対象端末でHTMLファイルを開く
2. 各ボタン/リンクをクリック
3. ブロックされるパターンとされないパターンを確認

## 関連設定（Chrome管理コンソール）

```
URLBlocklist: javascript:*
```

## 注意

本ファイルは検証目的です。フィルタリング回避を助長する意図はありません。
