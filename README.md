# 🎨 デザインシステム & HP/LP テンプレートリポジトリ

デザイン性に優れたホームページ（HP）とランディングページ（LP）を簡単に作成できるリポジトリです。
Claude Code の専門スキル（UI/UXデザイン、Webデザイン、X投稿最適化）を統合し、プロフェッショナルなWebサイト制作をサポートします。

## ✨ 特徴

- **プロフェッショナルなデザインシステム** - カラー、タイポグラフィ、スペーシング、コンポーネントを体系化
- **すぐに使えるテンプレート** - LP、HP用の完成度の高いテンプレート
- **Claude Code スキル統合** - UI/UX、Webデザイン、マーケティングの専門知識
- **レスポンシブ対応** - モバイルファーストで、すべてのデバイスに対応
- **アクセシビリティ対応** - WCAG準拠、誰でも使いやすいデザイン
- **カスタマイズ可能** - CSSカスタムプロパティで簡単にカスタマイズ

## 📁 プロジェクト構造

```
ピラティス/
├── .agents/                    # Claude Code エージェント設定
│   └── skills/                # 専門スキル
│       ├── ui-ux-design/      # UI/UXデザインスキル
│       ├── web-design/        # Webデザインスキル
│       └── x-viral-post/      # X投稿最適化スキル
│
├── design-system/             # デザインシステム
│   ├── index.css             # メインエントリーポイント
│   ├── colors.css            # カラーシステム
│   ├── typography.css        # タイポグラフィ
│   ├── spacing.css           # スペーシングシステム
│   └── components.css        # UIコンポーネント
│
├── templates/                 # テンプレート
│   ├── landing-page/         # ランディングページテンプレート
│   │   └── index.html
│   ├── homepage/             # ホームページテンプレート
│   └── components/           # 再利用可能コンポーネント
│
├── examples/                  # 使用例
│   └── pilates-lp/           # ピラティススタジオLP例
│       └── index.html
│
├── README.md                  # このファイル
└── package.json              # プロジェクト設定
```

## 🚀 クイックスタート

### 1. デザインシステムを使う

HTMLファイルに以下を追加：

```html
<link rel="stylesheet" href="design-system/index.css">
```

### 2. テンプレートを使う

```bash
# ランディングページテンプレートをコピー
cp templates/landing-page/index.html your-project/

# または、ピラティス例をベースにする
cp examples/pilates-lp/index.html your-project/
```

### 3. ブラウザで開く

```bash
# シンプルなローカルサーバーを起動（推奨）
npx http-server . -p 8080

# または直接HTMLファイルを開く
open templates/landing-page/index.html
```

## 🎨 デザインシステムの使い方

### カラーシステム

```html
<!-- プライマリカラー -->
<div style="background-color: var(--color-primary-600);">
  Primary Content
</div>

<!-- ユーティリティクラス -->
<div class="bg-primary text-white">
  Primary Background
</div>
```

利用可能なカラー：
- Primary: `--color-primary-{50-900}`
- Secondary: `--color-secondary-{50-900}`
- Neutral: `--color-neutral-{50-900}`
- Semantic: `--color-success`, `--color-error`, `--color-warning`, `--color-info`

### タイポグラフィ

```html
<h1>見出し1（最も大きい）</h1>
<h2>見出し2</h2>
<p class="lead">リード文</p>
<p>本文</p>

<!-- ユーティリティクラス -->
<p class="text-xl font-bold">大きく太字</p>
```

### スペーシング

```html
<!-- マージン -->
<div class="mt-4 mb-8">上に4、下に8のマージン</div>

<!-- パディング -->
<div class="px-6 py-12">左右6、上下12のパディング</div>

<!-- セクション -->
<section class="section">標準セクション（上下パディング付き）</section>
```

### コンポーネント

#### ボタン

```html
<button class="btn btn-primary">プライマリボタン</button>
<button class="btn btn-secondary">セカンダリボタン</button>
<button class="btn btn-ghost">ゴーストボタン</button>
<button class="btn btn-primary btn-lg">大きいボタン</button>
```

#### カード

```html
<div class="card">
  <div class="card-header">
    <h3 class="card-title">カードタイトル</h3>
    <p class="card-description">カードの説明文</p>
  </div>
  <div class="card-footer">
    <button class="btn btn-primary">アクション</button>
  </div>
</div>
```

#### フォーム

```html
<form>
  <div class="form-group">
    <label class="form-label">お名前</label>
    <input type="text" class="form-input" placeholder="山田 太郎">
    <span class="form-helper">ヘルプテキスト</span>
  </div>
  <button type="submit" class="btn btn-primary">送信</button>
</form>
```

#### グリッドレイアウト

```html
<div class="grid grid-cols-3 gap-8">
  <div class="card">カード1</div>
  <div class="card">カード2</div>
  <div class="card">カード3</div>
</div>
```

## 🤖 Claude Code スキルの使い方

このリポジトリには、以下のClaude Codeスキルが統合されています：

### UI/UX デザインスキル

```bash
# Claude Codeで以下のように依頼
"ui-ux-designスキルを使って、このボタンのインタラクションを改善して"
"ユーザビリティの観点から、このフォームをレビューして"
```

主な機能：
- ユーザー中心設計の原則
- インタラクションパターン
- アクセシビリティ対応
- レスポンシブデザイン

### Web デザインスキル

```bash
# Claude Codeで以下のように依頼
"web-designスキルを使って、モダンなヒーローセクションを作成して"
"この商品ページのビジュアル階層を改善して"
```

主な機能：
- モダンなレイアウトパターン
- タイポグラフィシステム
- カラーシステム
- パフォーマンス最適化

### X 投稿最適化スキル

```bash
# Claude Codeで以下のように依頼
"x-viral-postスキルを使って、このLPの告知投稿を作成して"
```

## 📝 カスタマイズ方法

### カラーのカスタマイズ

`design-system/colors.css`を編集：

```css
:root {
  /* あなたのブランドカラーに変更 */
  --color-primary-500: hsl(240, 70%, 55%);  /* ブルー */
  --color-secondary-500: hsl(320, 70%, 55%); /* ピンク */
}
```

### タイポグラフィのカスタマイズ

`design-system/typography.css`を編集：

```css
:root {
  /* フォントファミリーを変更 */
  --font-heading: 'Your Heading Font', sans-serif;
  --font-body: 'Your Body Font', sans-serif;
}
```

### コンポーネントのカスタマイズ

`design-system/components.css`で既存コンポーネントを上書き、または新規作成：

```css
.btn-custom {
  background: linear-gradient(135deg, #667eea, #764ba2);
  color: white;
  /* その他のスタイル */
}
```

## 🌟 実例

### ピラティススタジオLP

[examples/pilates-lp/index.html](examples/pilates-lp/index.html)

完全に機能するピラティススタジオのランディングページ例：
- カスタムカラースキーム（緑とゴールド）
- レスポンシブグリッドレイアウト
- インタラクティブなアニメーション
- お問い合わせフォーム
- 料金表、お客様の声など

ブラウザで開いて確認：
```bash
open examples/pilates-lp/index.html
```

## 🎯 使用例：新しいLPを作成

### ステップ1: テンプレートをコピー

```bash
cp templates/landing-page/index.html my-landing-page.html
```

### ステップ2: ブランドカラーをカスタマイズ

HTMLファイルの`<head>`内に追加：

```html
<style>
  :root {
    --color-primary-500: hsl(200, 70%, 50%);
    --color-secondary-500: hsl(280, 70%, 60%);
  }
</style>
```

### ステップ3: コンテンツを編集

- ヒーローセクションのテキストを変更
- 特徴セクションを自社の強みに変更
- 料金プランを更新
- フォームフィールドをカスタマイズ

### ステップ4: ブラウザで確認

```bash
open my-landing-page.html
```

## 🛠 開発ツール

### ローカルサーバー起動

```bash
npm start
# または
npx http-server . -p 8080
```

### ライブリロード付き開発サーバー

```bash
npm run dev
```

## 📚 参考リソース

### デザインシステム
- [スキルファイル: ui-ux-design](.agents/skills/ui-ux-design/SKILL.md)
- [スキルファイル: web-design](.agents/skills/web-design/SKILL.md)

### インスピレーション
- Linear (https://linear.app) - クリーンなデザイン
- Stripe (https://stripe.com) - 優れたタイポグラフィ
- Notion (https://notion.so) - シンプルで機能的

## 🤝 貢献

改善提案やバグ報告は大歓迎です！

## 📄 ライセンス

MIT License - 自由にご利用ください

## 💡 ヒント

1. **カスタムプロパティを活用** - CSS変数を使うことで、一箇所の変更で全体に反映
2. **モバイルファーストで考える** - 小さい画面から設計し、大きい画面に拡張
3. **アクセシビリティを忘れずに** - コントラスト、キーボード操作、スクリーンリーダー対応
4. **パフォーマンスを意識** - 画像最適化、遅延読み込み、CSSの最小化
5. **Claude Codeスキルを活用** - デザインレビューや改善提案に活用

## 🆘 サポート

質問や問題がある場合：
1. README.mdを確認
2. [examples/](examples/)フォルダのサンプルを参照
3. Claude Codeで該当スキルに質問

---

**Happy Coding! 🎉**

デザイン性に優れたWebサイトを作成して、ビジネスを成功させましょう！
