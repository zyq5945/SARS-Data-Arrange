
## 1.介绍说明

首先声明下，分析的中国SARS数据来源是百度搜索“site:china.com.cn title:通报全国内地非典型肺炎最新疫情(附表)”, 是由中国卫生部新闻办公室整理发布的表格数据（Google同样的搜索条件搜不出来），个人有点粗心大意，急急忙忙的可能什么地方搞错了也有极大可能性。

本项目是使用[diseasedataarrange](https://github.com/zyq5945/diseasedataarrange)程序，针对中国卫生部发布的SARS疫情和WHO总计SARS疫情，自动生成整理后的数据。


## 2.不同平台访问地址

针对可能对不同网站访问速度有快慢问题，酌情可以考虑以下最快的访问地址：


### 2.1 [2003年中国SARS（非典）数据](https://zyq5945.github.io/zyq5945/blog_10.html)

#### github.io 网站：[https://zyq5945.github.io/SARS-Data-Arrange/china](https://zyq5945.github.io/diseasedataanalysis/overview.html?StartTime=2003/4/22&MinDay=-116&MaxDay=120&DaysOfTreatment=32&DataUrl=https://zyq5945.github.io/SARS-Data-Arrange/china)

#### github.com 仓库：https://raw.githubusercontent.com/zyq5945/SARS-Data-Arrange/master/china


注：数据计算的开始时间点是2003/4/22。

注：其中子区域的死亡数重新映射为医疗人员病例数，想要查看医疗人员感染情况请自行将关系对应好。


### 2.2 [WHO全球SARS（非典）总计数据](https://www.who.int/csr/sars/country/table2004_04_21/en/)

#### github.io 网站：[https://zyq5945.github.io/SARS-Data-Arrange/area](https://zyq5945.github.io/diseasedataanalysis/overview.html?DataUrl=https://zyq5945.github.io/SARS-Data-Arrange/area)

#### github.com 仓库：https://raw.githubusercontent.com/zyq5945/SARS-Data-Arrange/master/area


注：数据计算的开始时间点是2003-02-27。

注：该数据没有详情/对比/仿真页面数据。


## 3.查看用于显示数据的HTML5项目

### [查看地址](https://github.com/zyq5945/diseasedataanalysis)


## 4.生成文件的说明

### 4.1 文件目录说明

| 目录名 |  说明 |
|---|---|
|  ChildDetail | 各个子按日期升序排序的详细情况目录，其下是各父名称目录，父目录下才是子文件 |
|  ParentDetail | 各个父按日期升序排序的详细情况目录 |
|  ParentLastChildren | 各个子按日期降序排序的最后更新情况目录，其下是各父名称目录，父目录下才是子文件 |


### 4.2 固定文件名称说明

| 文件名 |  说明 |
|---|---|
|  Total | 最后更新汇总的情况 |
|  LastParents | 最后更新的所有父情况 |
|  LastChildren | 最后更新的所有子情况 |


### 4.3 文件的各字段说明

注：标准化是指将值缩放到浮点数是0-1之间的值

| 字段 |  说明 |
|---|---|
|  TimeOffset | 浮点型的天数时间偏移 |
|  UpdateTime | 更新时间 |
|  ParentName | 父名称 |
|  ParentConfirmedCount | 父确诊数 |
|  ParentSuspectedCount | 父疑似数 |
|  ParentCuredCount | 父康复数 |
|  ParentDeadCount | 父死亡数 |
|  ParentTreatingCount | 父正在治疗数 |
|  ParentCuredRate | 父康复率 |
|  ParentDeadRate | 父死亡率 |
|  ParentTreatingRate | 父正在治疗率 |
|  ParentDeadDivideCured | 父死亡除以康复数 |
|  ParentCuredDivideDead | 父康复除以死亡数 |
|  ParentConfirmedNorm | 父确诊数标准化 |
|  ParentSuspectedNorm | 父疑似数标准化 |
|  ParentCuredNorm | 父康复数标准化 |
|  ParentDeadNorm | 父死亡数标准化 |
|  ParentTreatingNorm | 父正在治疗数标准化 |
|  ParentDeadDivideCuredNorm | 父确诊数标准化 |
|  ParentCuredDivideDeadNorm | 父康复除以死亡数标准化 |
|  ParentTatalConfirmedNorm | 总计的父确诊数标准化 |
|  ParentTatalSuspectedNorm | 总计的父疑似数标准化 |
|  ParentTatalCuredNorm | 总计的父康复数标准化 |
|  ParentTatalDeadNorm | 总计的父死亡数标准化 |
|  ParentTatalTreatingNorm | 总计的父正在治疗数标准化 |
|  ChildName | 子名称 |
|  ChildConfirmedCount | 子确诊数 |
|  ChildSuspectedCount | 子疑似数 |
|  ChildCuredCount | 子康复数 |
|  ChildDeadCount | 子死亡数 |
|  ChildTreatingCount | 子正在治疗数 |
|  ChildCuredRate | 子康复率 |
|  ChildDeadRate | 子死亡率 |
|  ChildTreatingRate | 子正在治疗率 |
|  ChildDeadDivideCured | 子死亡除以康复数 |
|  ChildCuredDivideDead | 子康复除以死亡数 |
|  ChildConfirmedCountRate | 子确诊数相对父占比率 |
|  ChildSuspectedCountRate | 子疑似数相对父占比率 |
|  ChildCuredCountRate | 子确康复数相对父占比率 |
|  ChildDeadCountRate | 子确死亡数相对父占比率 |
|  ChildTreatingCountRate | 子正在治疗数相对父占比率 |
|  ChildConfirmedNorm | 子确诊数标准化 |
|  ChildSuspectedNorm | 子疑似数标准化 |
|  ChildCuredNorm | 子康复数标准化 |
|  ChildDeadNorm | 子死亡数标准化 |
|  ChildTreatingNorm | 子正在治疗数标准化 |
|  ChildDeadDivideCuredNorm | 子确诊数标准化 |
|  ChildCuredDivideDeadNorm | 子康复除以死亡数标准化 |
|  ChildTatalConfirmedNorm | 总计的子确诊数标准化 |
|  ChildTatalSuspectedNorm | 总计的子疑似数标准化 |
|  ChildTatalCuredNorm | 总计的子康复数标准化 |
|  ChildTatalDeadNorm | 总计的子死亡数标准化 |
|  ChildTatalTreatingNorm | 总计的子正在治疗数标准化 |


## 5.数据排序问题

中文有多音字的情况，比如重庆的“重”可能会按读音zhòng来进行排序，所以排序会有些问题。

## 6.一些个人的DXY-COVID-19数据分析心得


[《使用OriginLab的Boltzmann模型拟合仿真预测中国COVID-19(2019-nCov)疫情康复情况》](https://zyq5945.github.io/zyq5945/blog_13.html)

----

**一些资料数据下载或者查看地址:**

[百度搜索中国卫生部新闻办公室关于通报全国内地非典型肺炎最新疫情](https://www.baidu.com/s?ie=utf-8&f=8&rsv_bp=1&rsv_idx=1&tn=baidu&wd=site%3Achina.com.cn%20title%3A%E9%80%9A%E6%8A%A5%E5%85%A8%E5%9B%BD%E5%86%85%E5%9C%B0%E9%9D%9E%E5%85%B8%E5%9E%8B%E8%82%BA%E7%82%8E%E6%9C%80%E6%96%B0%E7%96%AB%E6%83%85(%E9%99%84%E8%A1%A8)&rsv_t=019dfSk6Qnv5ClzTNrmN8NP%2FsYgNMo4XLVdU50bpxioZnL1QX3kRl8g0SZg&rsv_enter=1&rsv_dl=ib&rsv_sug3=2)

[非典（SARS，萨斯，沙士）是如何在天津爆发流行的？](http://blog.sina.com.cn/s/blog_8791cb400102vfv0.html)

[全国内地非典型肺炎疫情统计表（截至8月16日内地疫情）]( http://www.china.com.cn/chinese/zhuanti/feiyan/386427.htm)

[卫生部4月23日通报全国内地非典型肺炎最新疫情](http://www.china.com.cn/chinese/2003/Apr/319444.htm)

[卫生部5月18日通报全国内地非典型肺炎最新疫情](http://www.china.com.cn/chinese/2003/May/331415.htm)

[扒的原始表格数据地址在这下载](./data/SARS_China_Raw.xlsx)

[整理后的表格数据地址在这下载](./data/SARS_China.xlsx)

[百度百科---SARS事件](https://baike.baidu.com/item/SARS%E4%BA%8B%E4%BB%B6/7702261?fr=aladdin)

[维基百科---SARS事件]( https://zh.wikipedia.org/wiki/SARS%E4%BA%8B%E4%BB%B6)

