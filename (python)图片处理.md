# ��ͼ
cv2.line(img, pt1, pt2, color, thickness, lineType, shift)
'''
img, ����ͼ
pt1��ֱ���������
pt2, ֱ���յ�����
color, ��ǰ�滭����ɫ������BGRģʽ�£�����(255, 0, 0)��ʾ��ɫ���ʣ��Ҷ�ͼ�£�ֻ��Ҫ�������ȵ�������
thickness, ���ʵĴ�ϸ���߿�����-1��ʾ�����ͼ��������Բ��Ĭ��ֵ��1��
'''
# ���ƾ���
cv2.rectangle(image, start_point, end_point, color, thickness)
'''
image:����Ҫ�����ϻ��ƾ��ε�ͼ��
start:_point: ���Ǿ��ε���ʼ���ꡣ�����ʾΪ����ֵ��Ԫ�棬����x����ֵ��y����ֵ����
end����point: ���Ǿ��εĽ������ꡣ�����ʾΪ����ֵ��Ԫ�棬����x����ֵ��y����ֵ����
color�����ǻ�ֵ�þ��εı߽��ߵ���ɫ������BGR������ͨ��һ��Ԫ�档���磺��255��0��0��Ϊ��ɫ
thickness�����Ǿ��α߿�Ĵ�ϸ���ء����-1���ؽ���ָ������ɫ��������״
'''

# ����Բ
cv2.circle(image , center_coordinates, radius, color, thickness)
'''
center_cooedinates: ����Բ���������ꡣ
radius��Բ�İ뾶
'''

# �ı�д��
cv2.putText(image, text, org, font, fontScale, color, thickness)
'''
text:���Ƶ��ı��ַ�����Ӣ�� �����ţ�
org:����ͼ�����ı��ַ������½ǵ�����
font������ʾ�������͡�һЩ����������FONT_HERSHEY_SIMPLEX, FONT_HERSHEY_PLAIN��
fontScale������������ӳ���font-specific������С
'''

# ��������
form PIL import Image, ImageDraw, ImageFont
import cv2
import numpy as np

# cv2��ȡͼƬ
img = cv2.imread('shishi.jpg')# ���Ʋ����к���
cv2img = cv2.cvtColot(img, cv2.COLOR_BGR2RGB)
pilimg = image. formarry(cv2img)
#PILͼƬ�ϴ�ӡ����
draw = ImageDraw.Draw(pilimg) # ͼƬ�ϴ�ӡ
font = ImageFont.truetype("simehei.ttf", 20, encoding = "utf-8") # ����1�������ļ�·��������2�������С
draw.text((0, 0)"Hi,���ǣ�%", (255, 0, 0), font = font) # ����1�� ��ӡ���꣬����2���ı�������3�����С

# PILͼƬתcv2ͼƬ
cv2charimg = cv2.cvtColor(np.array(pilimg), cv2.COLOR_BGR2RGB)
# cv2.imshow("ͼƬ",cv2charimg)# ���ִ��ڱ�����ʾ����
cv2.imshow("phot", cv2charimg)

cv2.waitKey(0)
cv2.destroyAllWindows()