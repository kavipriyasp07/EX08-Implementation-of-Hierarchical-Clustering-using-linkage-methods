# EX8-Implementation of Hierarchical Clustering using linkage methods
## DATE:
## AIM:
To implement Hierarchical Clustering using single and complete linkage method

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Compute the distance matrix between all data points.
2.Identify the two closest cluster and merge them.
3.Update the distance matrix to reflect the new cluster.
4.Repeat steps 2 and 3 until only one cluster remains.

## Program:
```
/*
Program to implement Hierarchical Clustering using single and complete linkage method
Developed by:kavipriya S.P 
RegisterNumber: 2305002011 
*/
 import pandas as pd
 import numpy as np
 import matplotlib.pyplot as plt
 from scipy.cluster.hierarchy import dendrogram, linkage,fcluster
 from sklearn.preprocessing import StandardScaler
 import pandas as pd
 import numpy as np
 import matplotlib.pyplot as plt
 from scipy.cluster.hierarchy import dendrogram, linkage,fcluster
 from sklearn.preprocessing import StandardScaler
x = df[['StudentID','Marks']].values
x
z=linkage(x,method='complete')
plt.figure(figsize=(5,2))
plt.title("Dendogram for student segmentation")
labels=range(1,len(df)+1)
dendrogram(z,labels=labels)
plt.xlabel("Student ID")
plt.ylabel("Marks")
plt.show()
max_cluster=2
clusters=fcluster(z,max_cluster,criterion='maxclust')
clusters
plt.figure(figsize=(5,2))
plt.scatter(x[:,0],x[:,1],c=clusters,cmap='rainbow',s=100)
plt.title("Student segmented(Hierarchical clustering)")
plt.xlabel("Student ID")
plt.ylabel("Marks")
plt.show()
z=linkage(x,method='single')
plt.figure(figsize=(5,2))
plt.title("Dendogram for student segmentation")
labels=range(1,len(df)+1)
dendrogram(z,labels=labels)
plt.xlabel("Student ID")
plt.ylabel("Marks")
plt.show()
```

## Output:
![Screenshot 2024-10-17 131146](https://github.com/user-attachments/assets/22390058-6bd8-45d7-a323-89a462d02921)

![Screenshot 2024-10-17 131153](https://github.com/user-attachments/assets/5d9bb049-6277-431d-9d57-ee900df3f4cd)

![Screenshot 2024-10-17 131200](https://github.com/user-attachments/assets/897cde68-ccca-4060-b84a-ba9a450b696a)

![Screenshot 2024-10-17 131208](https://github.com/user-attachments/assets/407e8271-2014-4ae0-8995-996087deb2bc)

![Screenshot 2024-10-17 131220](https://github.com/user-attachments/assets/591d5a66-5b1d-4f13-8363-2ff5d9d39ff6)

![Screenshot 2024-10-17 131231](https://github.com/user-attachments/assets/367b45e9-6f57-409c-82d5-5840460e31b9)



## Result:
Thus the implementation of Hierarchical Clustering using single and complete linkage method in python programming and verified successfully.
