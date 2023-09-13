# watermark-generator
製作一個簡單的浮水印工具

```python
##加上浮水印
from PIL import Image
from PIL import ImageFont
from PIL import ImageDraw

def watermark_Image(img_path,output_path, text, pos):
    img = Image.open("/content/english.jpg") #打開路徑
    drawing = ImageDraw.Draw(img)
    black = (10, 15, 12)  ##調整色度
    drawing.text(pos, text, fill=black)
    img.show()
    img.save("/content/english.jpg")  #存放路徑

img = '/content/english.jpg'
watermark_Image(img, 'watermarked_2.jpg','Python', pos=(100, 100))  ##"Python表示你要印甚麼字上去"  POS是位置要放哪
```
