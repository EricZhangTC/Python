from matplotlib import pyplot as plt
x=range(2,26,2)
y=[15,13,14.5,17,20,25,26,26,24,22,18,15]
#设置图片大小
fig=plt.figure(figsize=(20,8),dpi=80)
#x轴个性化
_xtick_labels=[i/2 for i in range(2,49)]
plt.xticks(_xtick_labels[::3])
#画图
plt.plot(x,y)
#保存
#plt.savefig("./sig_size.png")
plt.show()


from matplotlib import pyplot as plt
import random
from matplotlib import font_manager

#windows和linux
#font=['family'='MicroSoft YaHei',
     #'weight'='bold',
     #'size'='larger']
#matplotlib.rc("font",**font)
#my_font=font_manager.Fontproperties(fname="字体地址")
x=range(0,120)
y=[random.randint(20,35) for i in range(120)]
fig=plt.figure(figsize=(20,8),dpi=80)
#调整x轴的刻度
_x=list(x)
#取步长，数字与字符串一一对应，数据的长度一样
_xticks_label=["10:{}".format(i) for i in range(60)]
_xticks_label+=["11:{}".format(i) for i in range(60)]
plt.xticks(_x[::5],_xticks_label[::5],rotation=45)#rotation表示旋转90度
plt.xlabel("time")
plt.ylabel("wendu")
plt.title("time-wendu")

plt.plot(x,y)
plt.show()
