# めんサポ 商品マスタ配信

アプリ(F-09)がここを見て商品データを更新します。

- `version.json` … `{"dataVersion": N}`。アプリはまずこれを取り、適用済みより新しいときだけ本体を取りに来ます
- `products.json` … マスタ本体

**手で編集しないでください。** 正はアプリ本体のリポジトリ `masterdata/products.json` で、
`tools/publish_master.py` が書き出します。

    python3 tools/publish_master.py --out <このリポジトリ>/mensapo/master

products.json → version.json の順に置き換わります(逆にすると、新バージョンを見たアプリが
古い本体を取りに行くため)。
