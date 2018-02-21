---
layout: post
title:  "常见函数及运算符号归纳"
date:   2016-08-22 00:00:00 +0800
categories: 技术相关
tag: R
---

* content
{:toc}



#常见函数及运算符号归纳  
##管理R工作空间的函数  
**getwd():** 显示当前的工作目录  
**setwd():** 修改当前的工作目录  
**ls():** 列出当前工作空间中的对象  
**rm():** 移除(删除)一个或多个对象  
**option():** 显示或设置当前选项  
**load():** 读取一个工作空间到当前会话中  
**q():** 退出R  

##处理数据的基本函数  
**class():** 查看数据类型  
**unclass():** 去掉变量的属性  
**exists():** 用来判断环境中是否存在某个对象  
**t():** 表示转置  
**diag():** 返回矩阵的对角线数值  
**names():** 给变量命名  
**dim():** 查看或设定某个对象的维度  
**rowSums():** 行和  
**rowMeans():** 行平均  
**colSums():** 列和  
**colMeans():** 列平均  
**length():** 显示对象中元素/成分的数量  
**intersect():** 取交集  
**union():** 取并集  
**str():** 显示某个对象的结构  
**cbind():** 按列合并对象，每个对象必须拥有相同的行数，且要以相同的排序顺序  
**rbind():** 按行合并对象，每个对象必须拥有相同的变量，不过它们的顺序不必一定相同  
**merge():** 横向合并两个数据框(数据集)，可以将两个数据框按某个或某几个共有变量进行合并  
**head():** 列出某个对象的开始部分(默认6行)  
**tail():** 列出某个对象的最后部分(默认6行)  
**newobject<-edit():** 编辑对象并另存为newobject  
**fix():** 直接编辑对象  
**any(is.na()):** 返回TRUE(FALSE)，表示有(无)缺失值  
**sum(is.na()):** 表示缺失值的个数  
**na.omit():** 移除所有含有缺失值的观测  
**sort():** 对数据进行排序，返回排好序的内容(默认升序)  
**order():** 对数据进行排序，返回排好序内容的下标(默认升序)  
**subset():** 选择变量和观测  
**sample():** 从数据集中(有放回或无放回地)抽取大小为n的一个随机样本  
**nchar():** 计算字符数量  
**substr():** 提取或替换一个字符向量中的子串  
**strsplit():** 分割字符向量中的元素  
**paste():** 连接字符串  
**toupper():** 大写转换  
**tolower():** 小写转换  
**length():** 对象的长度  
**seq(from,to,by):** 生成一个序列  
**rep(x,n):** 将x重复n次  
**cat():** 连接对象,输出的对象默认用空格分开。\n表示新行，\t为制表符，\'为单引号，\b为退格  
**cut():** 将数据进行切分

##逻辑运算符  
**<(>):** 小于(大于)  
**<=(>=):** 小于或等于(大于或等于)  
**==：** 严格等于  
**!=:** 不等于  
**!x:** 非x  
**x | y:** x或y  
**x & y:** x和y  

##数学运算符号及函数  
**x%%y:**x 除以y产生的余数  
**%\*%:** 矩阵乘法  
**x%in%y:** 判断x是否为y中的元素  
**solve(x,y):** 用来求解线性方程组，如果没有第二个参数输入，则会返回矩阵的逆
**abs():** 绝对值  
**sqrt():** 平方根  
**round(x,digits=n):** 将x四舍五入为指定位的小数  
**signif(x,digits=n):** 将x四舍五入为指定的有效数字位数  
**ceiling(x):** 不小于x的最小整数  
**floor(x):** 不大于x的最大整数  
**trunc(x):** 向0的方向截取的x中的整数部分  
**cos()、sin()、tan():** 余弦、正弦、正切  
**acos()、asin()、atan():** 反余弦、反正弦、反正切  
**cosh()、sinh()、tanh():** 双曲余弦、双曲正弦、双曲正切  
**acosh()、asinh()、atanh():** 反双曲余弦、反双曲正弦、反双曲正切  
**log(x,base=n):** 对x取以n为底的对数  
**log():** 自然对数，即ln()  
**exp():** 指数函数，即e^()  

##统计函数  
**mean():** 平均数  
**median():** 中位数  
**sd():** 标准差  
**var():** 方差  
**quantile(x,probs):** 求分位数。其中probs为一个由[0,1]之间的概率值组成的数值向量  
**range():** 求值域  
**sum():** 求和  
**diff(x,lag=n):** 滞后差分，lag用来指定滞后几项。默认的lag值为1  
**min():** 最小值  
**max():** 最大值  
**scale(x,center=TRUE,scale=TRUE):** 为数据对象x按列进行中心化(center=TRUE)或标准化(center=TRUE,scale=TRUE)  

##概率函数  
**形式：[dpqr]distribution_abbreviation():** d=密度函数，p=分布函数，q=分位数函数，r=生成随机数(随机偏差)  

<table class="table table-bordered table-striped table-condensed">
   <tr>
      <td>分布名称</td>
      <td>缩写</td>
      <td>分布名称</td>
      <td>缩写</td>
   </tr>
   <tr>
      <td>二项分布</td>
      <td>binom</td>
      <td>卡方分布</td>
      <td>chisq</td>
   </tr>
   <tr>
      <td>正态分布</td>
      <td>norm</td>
      <td>均匀分布</td>
      <td>unif</td>
   </tr>
   <tr>
      <td>t分布</td>
      <td>t</td>
      <td>F分布</td>
      <td>f</td>
   </tr>
   <tr>
      <td>泊松分布</td>
      <td>pois</td>
      <td>指数分布</td>
      <td>exp</td>
   </tr>
   <tr>
      <td>几何分布</td>
      <td>geom</td>
      <td>柯西分布</td>
      <td>cauchy</td>
   </tr>
   <tr>
      <td>Beta分布</td>
      <td>beta</td>
      <td>Gamma分布</td>
      <td>gamma</td>
   </tr>
   <tr>
      <td>Wilcoxon符号秩分布</td>
      <td>signrank</td>
      <td>Wilcoxon秩和分布</td>
      <td>wilcox</td>
   </tr>
</table>  