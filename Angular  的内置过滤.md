#### Angular  的内置过滤
##### 过滤器可以通过一个管道字符（|）和一个过滤器添加到表达式中。
> 1、 将小写字母转换成大写   uppercase
```
{{"asdasd" | uppercase}}
```
> 2 、将大写字母转换成小写    lowercase
```
{{'ADFDFF' | lowercase}}
```
> 3 、货币过滤器  默认在最前面增加$符号  
```
{{'1234567.432' | currrency:'￥'：3}}
<p>总价 = {{ (quantity * price) | currency:'￥'：3 }}</p>
currency：‘改变货币符号’:'保留几位小数'
```
> 4、 限制过滤器    limitTo
```
{{'北京欢迎你' |  limitTo:2}}
```
> 5 、 json格式过滤器
```
<pre>{{ {name:1,age:4} | json:4 }}</pre>
```
>6 、数字过滤器   number 
```
{{1234|number}}
```
> 7 、 日期过滤器   date
```
{{1489568089171 | date:"yyyy年MM月 hh:mm:ss"}}
```
> 8 、排序过滤器  orderBy
```
<tr ng-repeat="stu in students | orderBy:language:flag  track by $index">
orderBy:关键字段：升降序（true代表的是降序）默认是升序
```
> 9 、过滤器     filter
```
 <tr ng-repeat="stu in students | filter:{english:query} track by $index">
 filter可以指定查询{字段:查询条件} ，默认是全部
```