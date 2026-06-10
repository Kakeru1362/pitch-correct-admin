# RHC（Recruit Health Consulting） 運営入力コンソール

運営マスタ（Googleスプレッドシート）への入力をまとめた静的Webアプリ。
会議情報 / 企業情報 / 会計 を入力すると、GAS Web App 経由でスプシに自動保存される。

## 使い方
1. 公開URLを開く
2. 「設定」タブで GAS Web App URL（…/exec）を登録（初回のみ・端末に記憶）
3. 各タブで入力して登録

## gourmet.html — グルメさがしアプリ
食べログ風のグルメ検索アプリ（単一HTML・スマホ向け）。
- 店舗データ: OpenStreetMap Overpass API（実在の飲食店）
- 地図: Leaflet + OSM タイル / エリア検索: Nominatim
- 保存リスト・閲覧履歴・ネット予約（デモ）・口コミは端末内（localStorage）に保存
- `gourmet.html` をブラウザで開くだけで動作（GitHub Pages 等での公開も可）
