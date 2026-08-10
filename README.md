# Sodato — 製品LP

iPhone アプリ「Sodato」（内部名 PlantCareLog）の製品紹介ページ。GitHub Pages で公開する想定。

- 公開URL: https://shoheicraftdev-design.github.io/sodato-lp/
- App Store: **未確定**（審査中）。CTA は `<span class="cta-pending">App Store 審査中</span>` で待機中。
  承認後に `index.html` の2箇所（ヒーロー・フッター、各 `TODO` コメントの直下）を
  `<a class="cta" href="https://apps.apple.com/jp/app/id########">App Store で見る</a>` へ戻し、
  ヒーローの `.cta-note` から「まもなく公開します。」を削る。`.cta-pending` の CSS も不要になったら消してよい
- サポート / プライバシーポリシー / 利用規約: https://shoheicraftdev-design.github.io/sodato-support/

## 位置づけ

えも日LP（`emo-diary-lp`）と同じく、**匿名ライン（note・Xで製品名を出さない）を維持したまま
アプリ名とストアURLを出せるチャネル**。ASC のマーケティングURLに設定する。
サポート・法務ページは別リポジトリ `sodato-support` が持つ（ここには置かない）。

## 素材

`images/` のスクリーンショットは、アプリ側リポジトリ `plant-care-log` の
`docs/appstore/screenshots/iphone-6.7-1284x2778/` を長辺640pxへ縮小したもの。
差し替える場合は元の 1284×2778 から作り直すこと。`appicon.png` は
`PlantCareLog/Assets.xcassets/AppIcon.appiconset/AppIcon-1024.png` の縮小。

| ファイル | 元 |
| :--- | :--- |
| `shot-01.png` | `01_home-list.png` |
| `shot-02.png` | `02_care-picker.png` |
| `shot-03.png` | `03_care-timeline.png` |
| `shot-04.png` | `04_monthly-intervals.png` |
| `shot-05.png` | `05_settings-notification.png` |

## 文言のルール（アプリ側 `docs/appstore/v1-store-listing.md` の禁止事項を継承）

書いてはいけない:

- **「完全オフライン」「一切通信しない」** … CloudKit と StoreKit で Apple とは通信する。言えるのは「第三者に通信しない」まで
- **「枯れません」「枯らさない」の断定** … 効能の断定になる
- **「AI」「自動診断」「種類判定」** … 実装していない
- **「写真も同期されます」** … 同期しているのは写真の**参照**であって画像ではない
- **「タグ」「比較」** … Ver1 に無い

月別間隔のグラフ（インラインSVG）の数値は **`normal`（標準的）カテゴリの実値**（12/12/7/7/7/5/5/5/7/7/7/12 日）。
換算表の正本は `plant-care-log/docs/reference/watering-category-table.md`。アプリ側で表を変えたらここも直す。

⚠️ `shot-04`（月別間隔の編集画面）に写っている 7/7/4/4/4/3/3/3/4/4/4/7 は **`moist`（湿り気を好む）** の値で、
グラフの `normal` とは別カテゴリ。同じ数字だと思って揃えないこと。
