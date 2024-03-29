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
