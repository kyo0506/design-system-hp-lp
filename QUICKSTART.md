# 🚀 クイックスタートガイド

このガイドでは、5分でランディングページを作成する方法を説明します。

## ステップ1: 依存関係のインストール（オプション）

ローカルサーバーを使いたい場合：

```bash
npm install
```

## ステップ2: テンプレートを選ぶ

### オプションA: 汎用ランディングページ

```bash
cp templates/landing-page/index.html my-page.html
```

### オプションB: ピラティス例をベースにする

```bash
cp examples/pilates-lp/index.html my-page.html
```

## ステップ3: ブラウザで開く

### 方法1: 直接開く

```bash
open my-page.html
```

### 方法2: ローカルサーバーで開く（推奨）

```bash
npm start
# ブラウザで http://localhost:8080 が開きます
```

## ステップ4: カスタマイズ

### ブランドカラーを変更

HTMLファイルの`<head>`タグ内に追加：

```html
<style>
  :root {
    /* あなたのブランドカラー */
    --color-primary-500: hsl(200, 70%, 50%);   /* 青 */
    --color-secondary-500: hsl(280, 70%, 60%); /* 紫 */
  }
</style>
```

よく使われるカラー：
- **青系**: `hsl(200, 70%, 50%)`
- **緑系**: `hsl(160, 60%, 45%)`
- **オレンジ系**: `hsl(35, 85%, 60%)`
- **ピンク系**: `hsl(320, 70%, 55%)`
- **紫系**: `hsl(280, 70%, 60%)`

### コンテンツを変更

1. **ヒーローセクション**を探す：
   ```html
   <section class="hero">
   ```

2. **タイトルと説明文を変更**：
   ```html
   <h1 class="hero-title">
     あなたのキャッチコピー
   </h1>
   <p class="hero-description">
     あなたのサービスの説明
   </p>
   ```

3. **特徴セクション**を編集：
   ```html
   <section id="features">
   ```

4. **料金プラン**を更新：
   ```html
   <section id="pricing">
   ```

## ステップ5: 画像を追加

### プレースホルダー画像を置き換え

```html
<!-- Before -->
<img src="https://via.placeholder.com/600x400" alt="Placeholder">

<!-- After -->
<img src="images/your-photo.jpg" alt="Your Photo">
```

### 推奨画像サイズ

- **ヒーロー画像**: 1920x1080px
- **特徴アイコン**: 512x512px
- **カード画像**: 800x600px
- **プロフィール写真**: 400x400px

## Claude Code スキルの活用

このリポジトリは Claude Code と統合されています：

### UI/UXデザインの改善

```
「ui-ux-designスキルを使って、このフォームのユーザビリティを改善して」
```

### Webデザインの最適化

```
「web-designスキルを使って、レスポンシブ対応を強化して」
```

### X投稿の作成

```
「x-viral-postスキルを使って、このLPの告知ツイートを作成して」
```

## よくある質問

### Q: カラーを変更したのに反映されない

A: ブラウザのキャッシュをクリアしてください：
- Chrome/Edge: `Cmd+Shift+R` (Mac) / `Ctrl+Shift+R` (Windows)
- Safari: `Cmd+Option+R`

### Q: モバイルで表示が崩れる

A: `viewport`メタタグが設定されているか確認：
```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

### Q: フォントが表示されない

A: Google Fontsのリンクが正しく読み込まれているか確認：
```html
<link rel="stylesheet" href="design-system/typography.css">
```

## 次のステップ

1. [README.md](README.md) で詳細なドキュメントを確認
2. [examples/pilates-lp](examples/pilates-lp) で実例を参照
3. Claude Code スキルでデザインレビューを依頼

## トラブルシューティング

### CSSが適用されない

```html
<!-- パスを確認 -->
<link rel="stylesheet" href="design-system/index.css">

<!-- または絶対パス -->
<link rel="stylesheet" href="/design-system/index.css">
```

### JavaScriptが動かない

ブラウザの開発者ツール（F12）でエラーを確認してください。

---

それでは、素敵なランディングページを作成しましょう！ 🎉
