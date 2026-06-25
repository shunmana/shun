# 左右反転画像 生成プログラム flip.py

<span style="color: red;">赤い文字</span>

## 1.概要

引数で指定した画像の左右反転画像を作成する python 3 で動作するプログラムです。

## 2.ソースコード

```
# このプログラムは python3用です。
# あらかじめ pip install pillow をインストールしておきます。
from PIL import Image
import sys

#コマンドライン引数から入力画像と出力画像のファイル名を取得
input_image = sys.argv[1]
output_image = sys.argv[2]

# 画像の読み込み
img = Image.open(input_image)

# 画像の左右反転
img_flip = img.transpose(Image.FLIP_LEFT_RIGHT)

# 画像の保存
img_flip.save(output_image)
```

## 3.使い方

### 3.1.実行例
- コマンドラインフォーマット
  ```
  rython3 flip.py <input_image_path> <output_image_path>
  ```
- 利用例
  ```
  python3 flip.py input.jpg output.jpg
  ```

### 出力結果
- 以下のように入力画像の左右反転画像が出力されます。
  | 入力画像(input.jpg) | 出力画像(output.jpg) |
  | --- | --- |
  | <img width="1275" height="850" alt="input" src="https://github.com/user-attachments/assets/69059423-b409-4fff-8ddd-487b7c17142a" /> | <img width="640" height="468" alt="output" src="https://github.com/user-attachments/assets/c0293865-29b4-4417-a864-92ee5bb87414" /> |
以上



