# Studio MiiA ウェブサイト デプロイメントガイド

## サーバーアップロード用ファイル

`studio-miia-website.zip` をサーバーにアップロードしてください。

## アップロード方法

### 方法1: FTPでアップロード（一般的なレンタルサーバー）

1. FTPクライアント（FileZilla、Cyberduckなど）でサーバーに接続
2. `studio-miia-website.zip` をサーバーの公開ディレクトリ（public_html、www、htdocsなど）にアップロード
3. サーバー上でZIPファイルを解凍
4. または、ローカルで解凍してからフォルダの中身をアップロード

### 方法2: サーバーのコントロールパネルからアップロード

1. レンタルサーバーのコントロールパネルにログイン
2. ファイルマネージャーを開く
3. 公開ディレクトリに移動
4. `studio-miia-website.zip` をアップロードして解凍

### 方法3: GitHub Pagesで公開（無料）

```bash
# リモートリポジトリにプッシュ
git push origin main

# GitHub Pages設定
# 1. GitHubリポジトリの Settings > Pages に移動
# 2. Source で "Deploy from a branch" を選択
# 3. Branch で "main" と "/sites/shibuya-pilates" を選択
# 4. Save をクリック
```

## ファイル構成

```
studio-miia-website/
├── index.html              # トップページ
├── guide.html              # 利用規約ページ
├── reserve-line.html       # LINE予約ページ
├── reserve-hotpepper.html  # Hot Pepper予約ページ
├── thank-you.html          # 予約完了ページ
├── images/                 # 画像ファイル
│   ├── logo.png
│   ├── gallery-1.jpg
│   ├── gallery-2.jpg
│   └── ...
└── design-system/          # デザインシステム（CSS）
    ├── index.css
    ├── colors.css
    ├── typography.css
    ├── spacing.css
    └── components.css
```

## アップロード後の確認事項

1. ブラウザでサイトにアクセスして表示を確認
2. モバイル表示も確認（レスポンシブデザイン）
3. 各ページへのリンクが正しく動作するか確認
   - トップページ → 利用規約
   - 予約ボタン（LINE、Hot Pepper）
   - TOPへ戻るリンク

## トラブルシューティング

### 画像が表示されない場合
- `images/` フォルダがルートディレクトリと同じ階層にあるか確認
- ファイルのパーミッション（権限）を確認（644推奨）

### CSSが適用されない場合
- `design-system/` フォルダがルートディレクトリと同じ階層にあるか確認
- ブラウザのキャッシュをクリアして再読み込み

## 更新履歴

- 2026-03-31: Studio MiiA 1号店・2号店対応版リリース
  - 店舗情報更新（六本木ダイヤハイツ 510号・508号）
  - 利用規約ページデザイン刷新
  - Call CTAボタン削除
  - ギャラリー画像サイズ拡大

## サポート

技術的な質問や問題がある場合は、開発者にご連絡ください。
