import matplotlib
from matplotlib import pyplot as plt
import seaborn as sns
import pandas as pd
import math
import numpy as np
df=pd.read_csv("Documents\Cars93.csv")
df=df.head()
fig=plt.figure()
plt.title("Price Range of Car")
plt.boxplot(df["Price"])
#Interpreting the five summary
print(np.min(df.Price))
print(np.max(df.Price))
print(np.std(df.Price))
print(np.mean(df.Price))
print(np.median(df.Price))
Out Put
15.9
37.7
7.373031940796134
29.320000000000004
30.0
import matplotlib
from matplotlib import pyplot as plt
import pandas as pd
import math
import numpy as np
df=pd.read_csv("Documents\Cars93.csv")
df=df.head()
mode1=df['MPG.city'].mode()
print("Highest Frequency:",mode1)
fig=plt.figure()
x=df['MPG.city']
plt.title("Frequency distribution")
xlabel=['MPG.city']
plt.hist(x)
Highest Frequency: 0    18
1    19
2    20
3    22
4    25
Name: MPG.city, dtype: int64
(array([1., 1., 1., 0., 0., 1., 0., 0., 0., 1.]),
 array([18. , 18.7, 19.4, 20.1, 20.8, 21.5, 22.2, 22.9, 23.6, 24.3, 25. ]),
 <BarContainer object of 10 artists>)

RPM
import matplotlib
from matplotlib import pyplot as plt
import pandas as pd
df=pd.read_csv("Documents\Cars93.csv")
df=df.head()
fig=plt.figure()
x=df.Horsepower
y=df.RPM
plt.title("Scatter Plot")
plt.scatter(x,y)
<matplotlib.collections.PathCollection at 0x1e2465aad30>

x,y
import matplotlib
from matplotlib import pyplot as plt
import pandas as pd
df=pd.read_csv("Documents\Cars93.csv")
df=df.head()
fig=plt.figure()
x=df.EngineSize
y=df.Horsepower
plt.title("Variation between Engine Size and Horsepower")
plt.plot(x,y)
[<matplotlib.lines.Line2D at 0x1e246958940>]

import pandas as pd
import numpy as np
A=pd.Series([10,20,30,40,50])
B=pd.Series([40,50,60,70,80])
intersect=pd.Series(np.intersect1d(A,B))
print(intersect)
min=pd.Series(np.min(A))
print(min)
max=pd.Series(np.max(A))
print(max)
sum=pd.Series(np.sum(B))
print(sum)
0    40
1    50
dtype: int64
0    10
dtype: int64
0    50
dtype: int64
0    300
dtype: int64
​
