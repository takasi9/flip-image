# 左右反転画像生成プログラム flip.py

## 1. 概要

引数で指定した画像の左右反転画像を作成する python3 で動作するプログラムです。

## 2. ソースコード

```python
# このプログラムは python3用です。
# あらかじめ pip install pillow で pillow をインストールしておきます。

from PIL import Image
import sys

input_image = sys.argv[1]
output_image = sys.argv[2]

img = Image.open(input_image)

img_flip = img.transpose(Image.FLIP_LEFT_RIGHT)

img_flip.save(output_image)
```

## 3. 使い方

### 3.1 実行例

コマンドラインフォーマット

```bash
python3 flip.py <input_image_path> <output_image_path>
```

利用例

```bash
python3 flip.py input.jpg output.jpg
```

## 3.2 出力結果

以下のように入力画像の左右反転画像が出力されます。

|入力画像(input.jpg)|出力画像(output.jpg)|
|-|-|
|![input](input.jpg)|![output](output.jpg)|
