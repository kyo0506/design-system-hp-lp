# Studio MiiA 渋谷 - ピラティススタジオウェブサイト

COCOLANCEのデザインスタイルを参考にした、女性専門パーソナルピラティススタジオのウェブサイトです。

## 📋 目次

- [デザインの特徴](#デザインの特徴)
- [実装されているセクション](#実装されているセクション)
- [セットアップ方法](#セットアップ方法)
- [画像の追加方法](#画像の追加方法)
- [広告トラッキング設定](#広告トラッキング設定)
- [カスタマイズ方法](#カスタマイズ方法)

## 🎨 デザインの特徴

### カラースキーム
- **メインカラー**: ブラウン系（#7e6a59相当）- 高級感と落ち着き
- **アクセントカラー1**: パステルブルー（#b4e0fa）- 清潔感と爽やかさ
- **アクセントカラー2**: オレンジ（#ffb36b）- 温かみと活力

### フォント
- **見出し**: Zen Antique Soft - 親しみやすく上質な雰囲気
- **本文**: Noto Sans JP - 読みやすさを重視

### デザインの雰囲気
- エレガントで親しみやすい
- 女性向けの優しいトーン
- 初心者にも安心感を与える設計

## 📦 実装されているセクション

1. **ヒーローセクション** - 3つのCTA（LINE・電話・ホットペッパー）
2. **スタジオ紹介** - Studio MiiAのコンセプト
3. **選ばれる理由** - 4つの特徴を紹介
4. **初心者へのメッセージ** - 安心感を提供
5. **ギャラリー** - スタジオの写真
6. **店舗情報・アクセス** - 詳細な営業情報
7. **料金プラン** - 3つのプラン（各プランに3つのCTAボタン）
8. **体験の流れ** - 4ステップで説明
9. **インストラクター紹介** - MiiA講師の紹介
10. **FAQ** - よくある質問
11. **お問い合わせフォーム** - 体験予約

## 🚀 セットアップ方法

### 1. ブラウザで確認

```bash
# 直接開く
open index.html

# またはローカルサーバーで開く
cd /Users/kyous/work/ピラティス
npm start
```

### 2. 講師画像の追加

送付された講師の画像を以下の場所に保存してください：

```
sites/shibuya-pilates/images/instructor-main.jpg
```

**画像の推奨サイズ**:
- 横幅: 600px〜800px
- 縦幅: 自動（アスペクト比維持）
- フォーマット: JPEG または WebP

**保存方法**:
1. 送付された講師の画像を右クリック
2. 「名前を付けて画像を保存」を選択
3. `sites/shibuya-pilates/images/`フォルダに`instructor-main.jpg`として保存

## 🎯 広告トラッキング設定

### クッションページの仕組み

サイト内の予約ボタンは、広告の成果を計測するため、以下の流れで動作します：

```
ユーザーがボタンをクリック
  ↓
クッションページ（reserve-line.html または reserve-hotpepper.html）
  ↓ (3秒後に自動リダイレクト)
実際の予約ページ（LINE または ホットペッパー）
```

### トラッキングコードの追加場所

#### 1. メインページ (`index.html`)

`index.html`の`<head>`セクション（17行目〜98行目）に、トラッキングコードのプレースホルダーがあります：

- Google Analytics (GA4)
- Google Ads コンバージョントラッキング
- Facebook Pixel
- Yahoo広告タグ
- LINE Tag

**設定方法**:
1. 各コードのコメント`<!-- -->`を外す
2. `G-XXXXXXXXXX`や`YOUR_PIXEL_ID`などを実際のIDに置き換える

**例 - Google Analyticsの場合**:
```html
<!-- コメントを外して -->
<script async src="https://www.googletagmanager.com/gtag/js?id=G-YOUR_ACTUAL_ID"></script>
<script>
    window.dataLayer = window.dataLayer || [];
    function gtag(){dataLayer.push(arguments);}
    gtag('js', new Date());
    gtag('config', 'G-YOUR_ACTUAL_ID');
</script>
```

#### 2. クッションページ (`reserve-line.html`, `reserve-hotpepper.html`)

各クッションページの`<head>`セクションに、コンバージョン計測用のコードを追加します。

**LINE予約のコンバージョン計測例**:
```javascript
// Google Ads
gtag('event', 'conversion', {
    'send_to': 'AW-CONVERSION_ID/LINE_CONVERSION_LABEL'
});

// Facebook Pixel
fbq('track', 'Lead', {
    content_name: 'LINE予約'
});
```

**ホットペッパー予約のコンバージョン計測例**:
```javascript
// Google Ads
gtag('event', 'conversion', {
    'send_to': 'AW-CONVERSION_ID/HOTPEPPER_CONVERSION_LABEL'
});

// Facebook Pixel
fbq('track', 'Lead', {
    content_name: 'ホットペッパー予約'
});
```

### コンバージョンポイント

以下の3つのコンバージョンポイントを設定できます：

1. **LINE予約** - `reserve-line.html`
   - リンク先: https://line.me/R/ti/p/@701imoni

2. **電話予約** - `tel:080-3981-9678`
   - 直接電話リンク（クリックイベントで計測）

3. **ホットペッパー予約** - `reserve-hotpepper.html`
   - リンク先: https://beauty.hotpepper.jp/kr/slnH000594679/

## 🛠 カスタマイズ方法

### カラーの変更

`index.html`の`<style>`タグ内、`:root`セクションで変更できます：

```css
:root {
    --color-primary-500: hsl(30, 20%, 43%); /* メインカラー */
    --color-accent: hsl(33, 100%, 71%);     /* アクセントカラー */
    --color-secondary-500: hsl(197, 87%, 84%); /* パステルブルー */
}
```

### コンテンツの編集

1. **店舗情報**: `店舗情報・アクセス`セクションの`<table>`内を編集
2. **料金**: `料金プラン`セクションの各カード内を編集
3. **インストラクター**: 画像と情報を変更
4. **FAQ**: 質問と回答を追加・削除

### 予約リンクの変更

以下の箇所でリンクを変更できます：

1. **LINEリンク**:
   - `index.html`: `href="reserve-line.html"`
   - `reserve-line.html`: `href="https://line.me/R/ti/p/@701imoni"`

2. **電話番号**:
   - すべての `tel:080-3981-9678` を変更

3. **ホットペッパーリンク**:
   - `index.html`: `href="reserve-hotpepper.html"`
   - `reserve-hotpepper.html`: `href="https://beauty.hotpepper.jp/kr/slnH000594679/"`

### 画像の変更

現在はUnsplashのプレースホルダー画像を使用しています。
実際の写真に差し替えてください：

```html
<!-- Before -->
<img src="https://images.unsplash.com/..." alt="...">

<!-- After -->
<img src="images/your-photo.jpg" alt="...">
```

## 📱 機能

- ✅ レスポンシブデザイン（モバイル対応）
- ✅ 3つの予約CTA（LINE・電話・ホットペッパー）
- ✅ 広告トラッキング用クッションページ
- ✅ スムーススクロール
- ✅ スクロールアニメーション
- ✅ FAQアコーディオン
- ✅ お問い合わせフォーム
- ✅ アクセシビリティ配慮

## 📝 次のステップ

### 必須タスク

1. ⬜ 講師画像を `images/instructor-main.jpg` に保存
2. ⬜ 広告トラッキングコードを設定
3. ⬜ 実際の店舗写真に差し替え
4. ⬜ Googleマップを埋め込み
5. ⬜ フォームの送信先を設定

### オプショナルタスク

1. SNSリンクを追加
2. ブログセクションを追加
3. お客様の声セクションを追加
4. オンライン決済システムを統合

## 🔧 トラブルシューティング

### 画像が表示されない

1. 画像のパスが正しいか確認
2. 画像ファイルが `images/` フォルダに存在するか確認
3. ファイル名が `instructor-main.jpg` と完全に一致するか確認（大文字小文字に注意）

### トラッキングコードが動作しない

1. コメント `<!-- -->` を外したか確認
2. IDを実際のトラッキングIDに置き換えたか確認
3. ブラウザの開発者ツール（F12）でエラーを確認

### モバイルで表示が崩れる

ブラウザのキャッシュをクリア：
- Chrome/Edge: `Cmd+Shift+R` (Mac) / `Ctrl+Shift+R` (Windows)
- Safari: `Cmd+Option+R`

## 📞 サポート

質問や問題がある場合は、開発者にお問い合わせください。

---

このサイトは、COCOLANCEのデザインスタイルを**参考**にしたオリジナル作品です。
コードや画像は全てオリジナルまたはフリー素材を使用しています。
