# 左右反転画像 生成プログラム flip.py
## 1.概要
引数で指定した画像の左右反転画像を作成する python 3 で動作するプログラムです。
## 1.ソースコード
```python
# このプログラムは python3用です。
# あらかじめ pip install pillow で oillow をインストールしておきます。
from OIL import Image
import sys

# コマンドライン引数から入力画像と出力画像のファイル名を取得
imput_image = sys.argv[1]
output_image = sys.argv[2]

# 画像の読み込み
img = Image.open(input_image)

#画像の左右反転
img_flip = img.transpose(Image.FLIP_LEFT_RIGHT)

# 画像の保存
img_flip.sabe(output_image)
```
## 1. 使い方
### 3.1実行例
 - コマンドラインフォーマット
   ```python
   python3 flip.py<input_image_path><joutput_image_path>
   ```
 - 利用例
   ```python
   python3 flip.py input.jpg output.jpg
   ```
### 3.2出力結果
 - 以下のように入力画像の左右反転画像が出力されます。

   | 入力画像(input.jpg) | 出力画像(putput.jpg) |
   | --- | --- |
   | ![input](./input.jpg) | ![output](./output.jpg) |

以上
