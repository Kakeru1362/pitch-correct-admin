# RHC（Recruit Health Consulting） 運営入力コンソール

運営マスタ（Googleスプレッドシート）への入力をまとめた静的Webアプリ。
会議情報 / 企業情報 / 会計 を入力すると、GAS Web App 経由でスプシに自動保存される。

## 使い方
1. 公開URLを開く
2. 「設定」タブで GAS Web App URL（…/exec）を登録（初回のみ・端末に記憶）
3. 各タブで入力して登録

## alarm.html — サビ起き（ミュージックアラーム）
好きな曲のサビ（指定した秒数）から音楽が流れて起きるアラームアプリ（単一HTML・スマホ向け・Web試作版）。
- 音楽: 端末内の音楽ファイルを追加（IndexedDB に保存・リロード後も保持）
- サビ位置: 曲ごとに分・秒で指定、その位置から試聴可能
- アラーム: 時刻＋曜日で複数登録、ON/OFF、ラベル
- 鳴動: サビから再生・音量フェードイン・全画面表示
- 二度寝防止: 連続タップ or 計算問題で解除、スヌーズ対応
- 設定・サビ位置は端末内（localStorage / IndexedDB）に保存
- 要件は `alarm-requirements.md` を参照
- ⚠ Web版の制約: 画面ロック/タブを閉じると鳴らないことがある・自動再生制限あり（試作・操作感確認用）

## gourmet.html — グルメさがしアプリ
食べログ風のグルメ検索アプリ（単一HTML・スマホ向け）。
- 店舗データ: OpenStreetMap Overpass API（実在の飲食店）
- 地図: Leaflet + OSM タイル / エリア検索: Nominatim
- 保存リスト・閲覧履歴・ネット予約（デモ）・口コミは端末内（localStorage）に保存
- `gourmet.html` をブラウザで開くだけで動作（GitHub Pages 等での公開も可）
