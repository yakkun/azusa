# 特急あずさ 時刻表ガントチャート 🚆

[![GitHub Pages](https://img.shields.io/badge/GitHub%20Pages-Live%20Demo-brightgreen?style=flat-square&logo=github)](https://yakkun.github.io/azusa/)
[![Train](https://img.shields.io/badge/JR%20East-E353%E7%B3%BB-7b1fa2?style=flat-square)](https://yakkun.github.io/azusa/)
[![License](https://img.shields.io/badge/license-MIT-blue?style=flat-square)](LICENSE)

JR東日本の中央本線・篠ノ井線・大糸線を走る特急「あずさ」定期全16往復（下り16本・上り16本）の運行ダイヤを、直感的に可視化したモダンなガントチャートWebサービスです。

🌐 **公開URL:** [https://yakkun.github.io/azusa/](https://yakkun.github.io/azusa/)

---

## 📸 スクリーンショット

- **ダークモード（デフォルト）**: E353系の「あずさバイオレット」「アズサブルー」が映えるディープスレートUI
- **ライトモード**: E353系の「アルパインホワイト」車体を想起させるクリーンなUI

---

## ✨ 主な機能

### 1. 直感的なガントチャート運行ダイヤ
- **下り（松本・白馬方面）／上り（新宿・東京方面）切替**: パターンダイヤ（下り: 毎時00分発基準 / 上り: 毎時10分発基準）の全貌が一目で把握可能。
- **直通区間の一体表現**: 基本区間（新宿〜松本）に加え、東京発着・千葉発着・大糸線白馬直通の運行行程をシームレスに表示。
- **Stickyレイアウト**: 
  - 左端の**列車名列（号数・バッジ）が横スクロール時に常時固定**。
  - 上部の**時間軸ヘッダー（06:00〜24:00）が縦スクロール時に常時固定**。

### 2. 途中停車駅＆発着時刻タイムライン（ポップアップ）
- 各列車のバーまたは行をクリックすると、始発駅から終着駅までの**すべての途中停車駅と発着時刻**を縦型タイムラインでポップアップ表示。
- 新宿・八王子・甲府・塩尻・松本などの主要乗換駅には「主要駅」タグを付与。

### 3. E353系 窓枠回避＆車窓Tipsカード
- **上下線連動の座席選びガイド**:
  - **下り（松本方面）**: **奇数番席**（1, 3, 5, 7…番）が窓枠（ピラー）を避けてワイドな車窓を確保
  - **上り（東京方面）**: **偶数番席**（2, 4, 6, 8…番）が窓枠（ピラー）を避けてワイドな車窓を確保
- **車窓の景色ガイド**:
  - **D席**: 富士山（甲府手前・韮崎付近）、甲府盆地の夜景、南アルプス、諏訪湖側
  - **A席**: 八ヶ岳連峰（小淵沢〜茅野）、北アルプス連峰側

### 4. リアルタイム運行インジケーター（Now Line）
- 営業時間帯（06:00〜24:00）に、現在時刻の縦ラインとパルスバッジ（`NOW 14:35`など）を自動描画＆1分ごとにリアルタイム更新。

### 5. クイックフィルター ＆ インクリメンタル検索
- **ワンタップフィルター**: 「すべて」「東京発着」「千葉発着」「白馬直通」「最速達タイプ」
- **インクリメンタル検索**: 列車番号（「1号」「41号」）や時刻（「07:00」等）を入力して即座に絞り込み。

### 6. ダーク / ライト テーマ切替 & URL状態同期
- 右上の ☀️/🌙 ボタンで瞬時にテーマ切り替え（`localStorage` に自動保存）。
- `?dir=up&filter=tokyo&theme=light` など、URLクエリパラメータによる状態保持に対応（ブックマークや共有可能）。

---

## 🛠️ 技術スタック

- **フロントエンド**: HTML5, CSS3, Vanilla JavaScript（外部フレームワーク不要・単一HTMLファイル完結）
- **フォント**: 
  - [Inter](https://fonts.google.com/specimen/Inter)（UI欧文）
  - [Noto Sans JP](https://fonts.google.com/specimen/Noto+Sans+JP)（和文）
  - [JetBrains Mono](https://fonts.google.com/specimen/JetBrains+Mono)（時刻・等幅数字）
- **ホスティング**: GitHub Pages

---

## 🚀 ローカルでの実行

単一の静的HTMLファイルで構成されているため、クローンしてすぐにブラウザで利用できます。

```bash
git clone https://github.com/yakkun/azusa.git
cd azusa

# ブラウザで直接開く
open index.html

# またはローカルサーバーを起動する場合
python3 -m http.server 8000
# http://localhost:8000 にアクセス
```

---

## 📋 運行データについて

- **対象列車**: JR東日本 中央線特急「あずさ」定期全16往復（1号〜60号）
- **使用車両**: E353系（9両編成 / 12両編成、全車指定席）
- ※臨時延長列車や臨時便、季節運行日は各運行日の最新時刻表をご確認ください。

---

## 👤 作者

- **YAKKUN** ([@yakkun](https://github.com/yakkun))

---

## 📄 ライセンス

This project is licensed under the [MIT License](LICENSE).
