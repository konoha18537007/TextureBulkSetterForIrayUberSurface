# Texture Bulk Setter For Iray Uber Surface
DAZ Studio アドオン

## 概要
Surfaces ペインで選択中のマテリアル(複数可)に対し、PBR テクスチャのセットを一括で登録します。GUI ダイアログ上でファイルを一つ選択するだけで、チェックボックスが ON の全てのテクスチャに対し、事前に設定したファイル名サフィックスに基づいてテクスチャをセットします。

このアドオンは特にマテリアルプリセットを作成する際などに有用です。

![screen1](screen1.gif 'screen1')

このスクリプトは存在しないファイルが指定されたテクスチャに関しては処理をスキップしますので、使用しないテクスチャについてわざわざチェックを外す必要はなく、無視するだけでよいです。

サフィックスの定義は settings.json を編集することで変更可能です。

このスクリプトが対応しているテクスチャの一覧とデフォルトのサフィックスは下記の通りです。

| テクスチャ | サフィックス |
| ------- | ------ |
| Base Color | [No Suffix] |
| Translucency Color | [No Suffix] |
| Glossy Reflectivity | _s |
| Dual Lobe Specular Reflectivity | _s |
| Diffuse Roughness | _r |
| Glossy Roughness | _r |
| Metallicity | _m |
| Base Bump | _b |
| Normal Map | n |
| Displacement Strength | _h |
| Cutout Opacity | _o |

このスクリプトは **Iray Uber のみ** に対応しています。

DAZ Studio 4.15.0.2 Pro Public Build でしか動作確認していません。使用は自己責任で。

## 使用方法
1. 対象のオブジェクトを選択。

2. "Surfaces" ペインで対象のマテリアル(複数可)を選択。

3. このスクリプトを実行。実行方法の例：
  * "texture_bulk_setter_for_iray_uber_surface.dsa" を DAZ の Viewport 上にドラッグアンドドロップ。
  * Content Library で "texture_bulk_setter_for_iray_uber_surface.dsa" をダブルクリック。
    - ライブラリ内にこのスクリプトを置いておく必要があります。

4. "Choose Base File..." をクリックしてファイル名サフィックス無しのファイルを選択。
  * この選択の結果は、各テクスチャのファイル名とファイルパスを決定するためだけに用いられます。

5. 必要に応じて設定変更。
  * 使わないテクスチャについて、左端のチェックボックスのチェックを外す。
    - 指定されている名称のファイルが存在しない場合は、チェックの有無に関わらずスキップされるのでわざわざ外す必要はありません。
  * 手動でファイルを指定したいテクスチャがある場合は、 "Choose File..." を押して指定して下さい。

6. "Run" を押してテクスチャをセット。

## 応用
settins.json を編集することでサフィックスとデフォルトでチェックが入るか否かを変更できます。

* `enabled` キー : デフォルトでチェックを入れるか否か
* `suffix` キー : サフィックス

## インストール
* どこか好きな場所に置いて下さい。

## アンインストール
* スクリプトを削除して下さい。

## License
GPL-3.0 License 
