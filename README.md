# 寺門 諒太 プロフィール／事業実績ページ

`index.html` 1枚 + `logos/` の静的サイト。ビルド不要。

```
terakado-profile/
├─ index.html          本体（CSS込み・1枚完結）
├─ logos/              各事業のロゴ（SVG）
└─ README.md
```

## 掲載している事業とURL

| 事業 | URL | ロゴ |
|---|---|---|
| リフォーム補助金ナビ | https://reform-hojo.jp | `logos/reform.svg` |
| ReformLead（業者向けCRM） | https://reform-hojo.jp/for-business | `logos/reformlead.svg` |
| Claude Works | https://claudelab.jp | `logos/claudeworks.svg` |
| 合トレ（4資格） | https://goutore.jp | `logos/goutore-full.svg` |
| └ 宅地建物取引士 | goutore.jp/takken | `logos/goutore-takken.svg` |
| └ 行政書士 | goutore.jp/gyoseishoshi | `logos/goutore-gyosei.svg` |
| └ 賃貸不動産経営管理士 | goutore.jp/chintai | `logos/goutore-chintai.svg` |
| └ 国家資格キャリアコンサルタント | goutore.jp/career-consultant | （ロゴ未作成・テキスト表示） |
| KabuScreen（止まった事業） | https://kabuscreen.jp | `logos/kabuscreen.svg` |
| 在留ナビ（止まった事業） | 本番ドメイン未確定のためリンクなし | `logos/zairyu.svg` |

## GitHub Pages で公開する手順

1. GitHub で新しいリポジトリを作る（**Public**）— 名前は英数字とハイフンのみ（例: `profile`）
2. **`index.html` と `logos/` フォルダごと**リポジトリのルートに置いて push
3. **Settings → Pages** を開く
4. **Source** を `Deploy from a branch`、**Branch** を `main` / `/ (root)` にして Save
5. 1〜2分待つと `https://<ユーザー名>.github.io/<リポジトリ名>/` で公開される

> **ユーザー名だけのURL**（`https://<ユーザー名>.github.io/`）にしたい場合は、
> リポジトリ名を `<ユーザー名>.github.io` にしてください。

### 独自ドメインを使う場合

Settings → Pages → **Custom domain** にドメインを入力し、
DNS 側で `CNAME` を `<ユーザー名>.github.io` に向けます。HTTPS は自動で付きます。

## 確定済み

- 連絡先: **support@lexor.jp**
- リフォーム補助金ナビ: **月10万PV**（講義資料側も同じ数字に統一済み）
- M&Aの記載: **掲載可**（社名は非開示のまま。「複数社とM&A協議中」まで）

## 公開前に確認したいところ

| 場所 | 内容 |
|---|---|
| 肩書き | 「LEXOR 代表 ／ ノウンズ株式会社 CSO・CAIO」の表記が最新か |
| キャリコンのロゴ | `logos/` に用意できたら、該当箇所のテキストチップを `<img>` に差し替え |
| 在留ナビのURL | 公開して差し支えないURLがあれば `<a class="url">` を追加 |
| OGP画像 | 必要なら `<meta property="og:image">` を追加 |

## メンテナンス

- 色・フォントは `<style>` 冒頭の CSS 変数に集約。ここを変えれば全体が変わる
- ライト／ダーク両対応（閲覧者のOS設定に追従）。ロゴは白いチップに載せているのでダークでも読める
- フォントは Google Fonts の Noto Sans JP
- 講座スライドと同じトンマナ（`dojo-vibe-coding/slides/design.py` と同じ配色）
- ヒーローは2カラム（左=紹介文／右=運営サービスのロゴパネル）。900px以下で縦積み
- 実機確認済み: 1280px / 1920px / モバイル390px。すべて中央寄せ・横スクロールなし
