# Python
Python code
import time
s = time.clock()
file_content = []

with open('C:/Users/zzd/Desktop/data mining/Python/reads.txt') as f:
    file_content = f.readlines()
g=file_content[1::4]
h=map(list, zip(*g))
import matplotlib.pyplot as plt
a1=[]
a2=[]
a3=[]
a4=[]
for i in range(0,49,1):
    a1.append(h[i].count('A')/100000.0)
    a2.append(h[i].count('G')/100000.0)
    a3.append(h[i].count('C')/100000.0)
    a4.append(h[i].count('T')/100000.0)
plt.plot(a1)
plt.plot(a2)
plt.plot(a3)
plt.plot(a4)
t = time.clock()
print t-s
plt.show()
