# 全国交通咨询系统 by C++ on Linux
### 1.信息存储
- 利用邻接表存储城市信息与线路信息，比邻接矩阵更加高效。
### 2.主要数据结构

- Time，规范时间的输入输出格式
- VNode，头结点，用于建立顶点表，存储城市信息
- ArcNode，表结点，用于建立边表，存储弧指向的城市信息，以及线路信息
- InfoType，存储线路信息
- priority queue，优先队列，用于优化 Dijkstra 算法时的插入结点以及取出到达对应点的最小权值
### 3.主要函数功能以及简介
- 查询城市编号：头结点建立顶点表时存储的是城市对应的序号
- 手动添加城市
- 从文件读取以添加城市
- 删除城市：删除城市时需要删除与该城市相关的所有线路
- 输出所有城市
- 更新城市列表：当新建城市个数加原本已存在城市个数大于 MAXSIZE 时，需要开辟空间存储新城市并 ++MAXSIZE
- 手动添加线路
- 插入线路：由于线路信息存于表结点里，所以需要新建表结点并加入对应起始城市的边表
- 从文件中读取线路
- 删除线路
- 求最少花费路径
- 求最少时间路径
### 4.核心算法 dijkstra 分析
- 如果想理解我代码中的核心算法部分，推荐看一下我的博客，博文里有本项目运用 dijkstra 算法的分析。博文链接：[dijkstra 最小路径算法](http://www.cnblogs.com/Bw98blogs/p/8205445.html "dijkstra 最小路径算法")
### 5.项目的总结性报告
- 我在文件夹 [Report](https://github.com/bw98/National-Transport-Advisory/tree/master/Report "Report") 里放了关于这次项目的设计思路以及函数的主要功能、数据流程图，如果对我项目的部分细节有疑惑，可以 clone 后仔细阅读 report.pdf
### 6.截图
![部分线路截图](https://images2017.cnblogs.com/blog/1199740/201801/1199740-20180105114038628-1177620256.png "部分线路截图")



[1]: http://www.cnblogs.com/Bw98blogs/p/8205445.html "dijkstra最小路径算法"
