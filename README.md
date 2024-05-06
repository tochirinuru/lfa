# 日本地形ガイドMAP
日めくり地形MAPサイトのソースコードです。

## サイトの基本情報
- サイト名: 日本地形ガイドMAP
- URL: https://tochirinuru.com/maps/lfa/
![image](https://github.com/tochirinuru/lfa/assets/102892587/bdd4840e-1a11-495f-a316-7a7f27213540)

## サイトの概要および詳細
- Xポスト（Twitterツイート）上で日本の地形を簡単に解説している地点を表示するWeb地図サイトです。
- 詳細については下記ページを参照してください。
- URL: https://tochirinuru.com/maps/lfa/overview.html

## ディレクトリ・ファイル構成
- /（root）
  - `gsi-dem-terrain.js`: 地理院標高タイルをMaplibre GL JSで扱うための定義
    - 参照URL: https://qiita.com/Kanahiro/items/8306e60e87746ca8a584
  - `gsi-std.json`: 地理院標準地図の定義
  - `index.html`: Web地図の表示
  - `overview.html`: サイトの説明
  - `style.css`: CSSの定義
- geofiles/
  - 地形解説地点を示すPMTilesおよびGeoJSONファイルの格納
- img/
  - アイコン画像ファイルの格納
- mapimg/
  - 地形解説ポップアップで使用する画像ファイルの格納

## ライブラリ
- MapLibre GL JS Ver.3.2.0
  - URL: https://maplibre.org/projects/maplibre-gl-js/

## ソース
### ベースマップ
- 国土地理院（地理院地図Vector提供実験）
  - 標準地図
    - URL: https://github.com/gsi-cyberjapan/gsimaps-vector-experiment

### 標高データ
- 国土地理院（標高タイル）
  - 地理院標高タイル
    - URL: https://maps.gsi.go.jp/development/demtile.html
    - 数値情報（国土基本情報）基盤地図情報（数値標高モデル）
    - 測量法に基づく国土地理院長承認（使用）R 5JHs 268

### レイヤ
- 国土地理院（ベクトルタイル提供実験）
  - 地形分類（自然地形）
    - URL: https://www.gsi.go.jp/bousaichiri/lfc_index.html
    - ※ベクトルタイルデータは2024年3月25日時点
  - 地形分類（人工地形）
    - URL: https://www.gsi.go.jp/bousaichiri/lfc_index.html
    - ※ベクトルタイルデータは2023年10月25日時点

- 国土地理院（地理院タイル）
  - 空中写真
    - URL: https://maps.gsi.go.jp/development/ichiran.html#seamlessphoto
  - 陰影起伏図
    - URL: https://www.gsi.go.jp/bousaichiri/hillshademap.html
  - 傾斜量図
    - URL: https://www.gsi.go.jp/bousaichiri/slopemap.html
  - 色別標高図
    - URL: https://cyberjapandata.gsi.go.jp/legend/attension_relief.html
  - 治水地形分類図 更新版（2007年以降）
    - URL: https://cyberjapandata.gsi.go.jp/legend/lcmfc2_legend.jpg
  - 明治期の低湿地
    - URL: https://cyberjapandata.gsi.go.jp/legend/lw_legend.pdf
  - 活断層図（都市圏活断層図）
    - URL: https://www.gsi.go.jp/common/000084060.pdf
  - 数値情報25000（土地条件）
    - URL: https://cyberjapandata.gsi.go.jp/legend/lcm25k_2012/lc_legend.pdf

## 更新履歴
- 2024-05-06（Ver.1.0.0）: サイト公開
