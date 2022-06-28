# 绘图
cv2.line(img, pt1, pt2, color, thickness, lineType, shift)
'''
img, 背景图
pt1，直线起点坐标
pt2, 直线终点坐标
color, 当前绘画得颜色。如在BGR模式下，传递(255, 0, 0)表示蓝色画笔，灰度图下，只需要传递亮度递增即可
thickness, 画笔的粗细，线宽。若是-1表示画封闭图像，如填充的圆。默认值是1。
'''
# 绘制矩形
cv2.rectangle(image, start_point, end_point, color, thickness)
'''
image:他是要在其上绘制矩形的图像
start:_point: 他是矩形的起始坐标。坐标表示为两个值的元祖，即（x坐标值，y坐标值）。
end——point: 他是矩形的结束坐标。坐标表示为两个值的元祖，即（x坐标值，y坐标值）。
color：他是会值得矩形的边界线的颜色。对于BGR，我们通过一个元祖。例如：（255，0，0）为蓝色
thickness：他是矩形边框的粗细像素。厚度-1像素将以指定的颜色填充矩形形状
'''

# 绘制圆
cv2.circle(image , center_coordinates, radius, color, thickness)
'''
center_cooedinates: 他是圆的中心坐标。
radius：圆的半径
'''

# 文本写入
cv2.putText(image, text, org, font, fontScale, color, thickness)
'''
text:绘制的文本字符串（英文 加引号）
org:他是图像中文本字符串左下角的坐标
font：他表示字体类型。一些字体类型是FONT_HERSHEY_SIMPLEX, FONT_HERSHEY_PLAIN等
fontScale：字体比例因子乘以font-specific基本大小
'''

# 中文输入
form PIL import Image, ImageDraw, ImageFont
import cv2
import numpy as np

# cv2读取图片
img = cv2.imread('shishi.jpg')# 名称不能有汉字
cv2img = cv2.cvtColot(img, cv2.COLOR_BGR2RGB)
pilimg = image. formarry(cv2img)
#PIL图片上打印汉字
draw = ImageDraw.Draw(pilimg) # 图片上打印
font = ImageFont.truetype("simehei.ttf", 20, encoding = "utf-8") # 参数1：字体文件路径，参数2：字体大小
draw.text((0, 0)"Hi,我是￥%", (255, 0, 0), font = font) # 参数1： 打印坐标，参数2：文本，参数3字体大小

# PIL图片转cv2图片
cv2charimg = cv2.cvtColor(np.array(pilimg), cv2.COLOR_BGR2RGB)
# cv2.imshow("图片",cv2charimg)# 汉字窗口标题显示乱码
cv2.imshow("phot", cv2charimg)

cv2.waitKey(0)
cv2.destroyAllWindows()