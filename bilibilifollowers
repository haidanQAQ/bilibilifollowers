# coding=utf-8
import re
import pygame
import requests

pygame.init()
url = "https://api.bilibili.com/x/relation/stat?vmid=8937720&jsonp=jsonp"  # 将8937720改为你的uuid
response = requests.get(url)
response.encoding = 'utf-8'
data = re.findall(r'\b\d+\b', response.text.lstrip('{"code":0,"message":"0","ttl":1,"data":{"id":').rstrip("}"))
text = "Followers:%s" % (data[4])
font = pygame.font.SysFont('arial', 256)  # 字体大小256
rtext = font.render(text, True, (0, 0, 0), (255, 255, 255))  # 默认RGB 255.255.255

pygame.image.save(rtext, "D:/followers.jpg")  # D盘为默认路径,followers.jpg为默认名
