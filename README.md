
# CHD_ListView_Structure
## 前言
大多数的iOS工程中，50%以上的页面是由**UITableView**或**UICollectionView**搭建的，这里统称为**ListView**。当我们接手已有项目时，我们如何快速的理清每个**ListView**的结构。或者，当我们自己写的某个页面过去很长时间时，产品过来告诉我们某个页面的某个位置需要调整，可能自己也是依稀记得哪部分是段头，哪部分是断尾，总要花一些时间来对应相应的区块。**CHD_ListView_Structure**正是为了让你快速的区分每个**ListView**的页面结构而生的。
## 使用
#### 方式一
直接下载源代码，在**Appdelegate**导入h文件，然后调用
``` 
[CHD_ListView_Structure openStructureShow_TableV:YES collectionV:YES]; 
```
即可。
#### 方式二
```
pod 'CHD_ListView_Structure'
```
然后导入头文件并调用上面的方法。
## 特征
* 支持**UITableView**和**UICollectionView**结构查看
* 支持只查看二者中一个，关闭另一个
* 无侵入，无需继承，一句话开启关闭
* 无论开启或关闭，只在**DEBUG**模式下生效
* **Header**、**Cell**、**Footer**使用不同颜色线框包围，并在其上展示类名及其**Index**
* 提供一个简单的可拖动的**Toggle**按钮，实时隐藏或显示**ListView**的结构(未开启时**Toggle**不会生效)
* 简单的内存泄漏判断依据（点击**Toggle**按钮时会打印当前存活的**ListView**总个数，当你返回到上一页面再次点击**Toggle**按钮时，如果个数未减少，那么可能存在内存泄漏）
## 效果
#### 1、百思不得姐(高仿)
对开源项目[百思不得姐(高仿)](https://github.com/targetcloud/baisibudejie)做了结构分析，其中部分效果图如下:
![baisi1](https://ws2.sinaimg.cn/large/006tKfTcly1fj8hygcal1j30fo0t2q70.jpg)
![baisi2](https://ws4.sinaimg.cn/large/006tKfTcly1fj8i4ha57fj30fo0t2jw1.jpg)
![baisi3](https://ws3.sinaimg.cn/large/006tKfTcly1fj8i6p841cj30fo0t2tc9.jpg)
![baisi4](https://ws4.sinaimg.cn/large/006tKfTcly1fj8i947v8tj30fo0t2djt.jpg)

#### 2、腾讯新闻
借助神奇的工具[IPAPatch](https://github.com/Naituw/IPAPatch)来看下大厂是如何使用tableView的,部分页面如下:
![TX1](https://ws1.sinaimg.cn/large/006tKfTcly1fj9mgzkcy6j30ku112dl7.jpg)
![TX2](https://ws1.sinaimg.cn/large/006tKfTcly1fj9n1k901xj30ku112wj7.jpg)
![TX3](https://ws4.sinaimg.cn/large/006tKfTcly1fj9n2ogosej30ku112teq.jpg)
![TX4](https://ws4.sinaimg.cn/large/006tKfTcly1fj9nnz1d97j30ku112tc9.jpg)

## 其他
如有问题，还请指正，共同进步。如果对您有所帮助，希望给颗✨✨(即使现在不用，收藏起来也是极好的)
## LICENSE
MIT
