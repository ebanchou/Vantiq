# 修改UTC时间为北京时间的方法
VANTIQ平台上使用的默认时间为UTC时间，如果需要改变UTC时间为本地时间，有两种方法
* 本地函数转换的方式；
* 使用地图平台提供的API进行转换
## 本地函数转换
具体函数如下：  
PROCEDURE BJTime()  
var ems = date(now(), "date", "epochSeconds")  
ems = ems+28800  
var bjTime = date(ems, "epochSeconds", "date")  
var newDate = parseDate(bjTime, "")  
return newDate  
