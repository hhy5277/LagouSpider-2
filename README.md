# 拉勾网多线程数据爬虫
## 项目简介 
基于java的拉勾网数据爬虫,通过封装后的HttpClient多线程抓取职位信息，公司信息等，并通过MyBatis框架实现数据持久化。

## 功能介绍
利用爬虫爬取40多个城市的技术类岗位信息，用于分析当前最新的就业行情

1. 各城市薪资以及职位数量对比，选择适合的就业城市
2. 不同技术岗位数量对比，选择最合适的就业方向
3. 输入职位关键字和城市，迅速锁定该城市就业最火的行政区和商区

## 分析报告
2016年5月，通过本爬虫抓取了拉勾网12W多条岗位信息，并进行统计分析，用Echarts做了图表。
[点击查看分析报告](http://www.codinghx.com/lagou/report.html)

## 使用方法
下载本项目到本地，并通过项目的sql文件创建MySQL表，然后运行相应的爬虫即可。

* PositionSpider.java --- 抓取全国40多个城市的所有技术类岗位
* AddressSpider.java --- 抓取指定城市下某个岗位在各行政区/商区的招聘数量并排序 
* CompanySpider.java --- 抓取全国的互联网公司信息（未完成）
* DetailsSpider.java --- 完善PositionSpider抓取的岗位信息，补充职位描述和职位详细地点等信息。	
