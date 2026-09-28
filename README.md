# Sodato — 製品LP

iPhone アプリ「Sodato 観葉植物の水やり記録」（ホーム画面の表示名は Sodato、内部名 PlantCareLog）の製品紹介ページ。GitHub Pages（main）で公開している。

- 内容の版: **ver-2.0（ストア 2.0・2026-09-16 公開）**。2026-09-28 に更新（d-yso5qm）
- 文言の正本: アプリ側リポジトリ `plant-care-log` の `docs/appstore/asc-paste/`（`description.txt`＝CEO が ASC で手直しした後の実値。公開中の説明文と一致）・`docs/appstore/ver-2.0-submission.md`・`docs/appstore/v2-store-listing.md`。LP で新しい言い回しを作らず、ここに揃える

- 公開URL: https://shoheicraftdev-design.github.io/sodato-lp/
- App Store: **公開中**。`https://apps.apple.com/jp/app/id6798340201`
  （2026-08-24、`index.html` 2箇所を `<a class="cta">` に差し替え済み）
- サポート / プライバシーポリシー / 利用規約: https://shoheicraftdev-design.github.io/sodato-support/

## 位置づけ

えも日LP（`emo-diary-lp`）と同じく、**匿名ライン（note・Xで製品名を出さない）を維持したまま
アプリ名とストアURLを出せるチャネル**。ASC のマーケティングURLには**設定していない**（空欄のまま。
`plant-care-log/docs/appstore/v2-store-listing.md` §8。入れる場合はその決定をアプリ側に記録してから）。
サポート・法務ページは別リポジトリ `sodato-support` が持つ（ここには置かない）。

## 素材

`images/` のスクリーンショットは、アプリ側リポジトリ `plant-care-log` の
`docs/appstore/screenshots/v2/iphone-6.7-1284x2778/`（ver-2.0 の掲載スクショ・上部にキャプション1行入り）を
長辺640pxへ縮小したもの（`sips -Z 640`）。
差し替える場合は元の 1284×2778 から作り直すこと。`appicon.png` は
`PlantCareLog/Assets.xcassets/AppIcon.appiconset/AppIcon-1024.png` の縮小。

| ファイル | 元 |
| :--- | :--- |
| `shot-01.png` | `01_home-list.png` |
| `shot-02.png` | `02_care-picker.png` |
| `shot-03.png` | `03_care-timeline-all.png`（全植物横断タイムライン） |
| `shot-04.png` | `04_monthly-intervals.png` |
| `shot-05.png` | `05_settings-notification.png` |

## 文言のルール（アプリ側 `docs/appstore/v1-store-listing.md` の禁止事項を継承。ver-2.0 の差分は `v2-store-listing.md`）

書いてはいけない:

- **「完全オフライン」「一切通信しない」** … CloudKit と StoreKit で Apple とは通信する。言えるのは「第三者に通信しない」まで
- **「枯れません」「枯らさない」の断定** … 効能の断定になる
- **「AI」「自動診断」「種類判定」** … 実装していない
- **「写真も同期されます」** … 同期しているのは写真の**参照**であって画像ではない
- **「タグ」「比較」** … Ver1 に無い

月別間隔のグラフ（インラインSVG）の数値は **`normal`（標準的）カテゴリの実値**（12/12/7/7/7/5/5/5/7/7/7/12 日）。
換算表の正本は `plant-care-log/docs/reference/watering-category-table.md`。アプリ側で表を変えたらここも直す。

⚠️ `shot-04`（月別間隔の編集画面）に写っている 7/7/4/4/4/3/3/3/4/4/4/7（キャプション「夏は3日、冬は7日」）は **`moist`（湿り気を好む）** の値で、
グラフの `normal` とは別カテゴリ。同じ数字だと思って揃えないこと。
