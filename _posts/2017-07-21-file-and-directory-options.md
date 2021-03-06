---
layout: post
title:  "文件与目录的常用基本操作"
date:   2017-07-21 00:00:00 +0800
categories: 技术相关
tag: Linux
---

* content
{:toc}




## 目录的特殊表示
**.** 代表此层目录  
**..** 代表上一层目录  
**-** 代表前一个工作目录  
**～** 代表目前用户身份所在的主文件夹  
**～account** 代表account这个用户的主文件夹

## 常用命令
**cd:** 切换目录  
**pwd:** 显示当前目录  
**mkdir:** 新建一个新的目录

```text
mkdir [-mp] 目录名称
参数：
-m: 配置权限（r:4, w:2, x:1）
-p: 递归创建所需要的目录（包含上层目录，若没有该参数，只能一层一层地创建）
```

**rmdir:** 删除一个空的目录

```text
rmdir [-p] 目录名称
参数：
-p: 连同上层的空目录也一起删除
```

**ls:** 查看文件与目录

```text
ls [-adhlrSt] 目录名称
参数：
-a: 全部文件，包括隐藏文件
-d: 仅列出目录本身，而不是列出目录内的文件数据
-h: 将文件容量以易读的方式（如GB,KB等）列出来
-l: 列出文件的属性与权限等详细数据
-r: 将排序结果反向输出
-S: 以文件容量大小排序，而不是以文件名排序
-t: 以时间排序，而不是以文件名排序
```

**cp:** 复制文件或目录

```text
cp [-adfipr] 源文件 目标文件
cp [options] 源文件1 源文件2 ... 目标目录
参数：
-a: 相当于pdr
-d: 若源文件为连接文件的属性，则复制连接文件属性而非文件本身
-f: 强制复制，若目标文件已存在且无法开启，则删除后再尝试一次
-i: 若目标文件已存在，在覆盖时会先询问操作的进行
-p: 连同文件的属性一起复制，而非使用默认属性
-r: 递归复制，用于目录的复制行为
```

**rm:** 移除文件或目录

```text
rm [fr] 文件或目录
参数：
-f: 强制删除，忽略不存在的文件，不会出现警告信息
-r: 递归删除，最常用在目录的删除
```

**mv:** 移动文件与目录或重命名

```text
mv [-f] 源文件 目标文件
mv [options] 源文件1 源文件2 ... 目标目录
参数：
-f: 强制复制，如果目标文件已存在，不会询问而直接覆盖
```

**cat:** 由第一行开始显示文件的内容

```text
cat [-nTv] 文件
参数：
-n: 打印出行号，空白行也有
-T: 将[Tab]按键以^I显示出来
-v: 列出一些看不出来的特殊字符
```

**head:** 显示前面几行

```text
head [-n number] 文件
参数：
-n: 后面接数字，代表显示几行，默认显示前10行
```

**tail:** 显示后面几行

```text
tail [-n number] 文件
参数：
-n: 后面接数字，代表显示几行，默认显示最后10行
```

**file:** 查看文件类型