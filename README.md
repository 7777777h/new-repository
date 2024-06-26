# Github

## 关键字查询
   awesome 去此标签类别中查询项目
   
   python tutorial 查询资料、书籍、文档
   
   socket sample 查询对应技术的文本

## Github 三要素
1. Respository 仓库
   
   仓库是github项目管理存储的基本单位
   
   一个仓库中存储一个项目，一个用户可以拥有多个仓库
   
   一般仓库分为public,private
2. Commit 提交
   1. 程序员在整个开发周期有大量的对代码资源的迭代和修改，都可以通过commit的方式      进行记录，便于程序员回溯代码，即使这些代码被删除
   2. 提交便于使用者观察者观察整个工程的开发流程及设计流程
3. Branch分支
   
   仓库中可以包含多个分支，分支才是代码文件的第一存储单位
   
   默认的仓库主分支为master/main

## 仓库内容
Code : 资源存储，代码存储，二进制，项目管理脚本，许可证等

issues : 使用时遇到的bug，提交，反馈

README : 使用markdown语言编写，工程的自述文件，开发进度，版本更新，使用介绍等

LICENSE : GPL 2.0 3.0 /Apahce 2.0 /Mit (放心用）
          这些许可证给使用者最大使用权限以及最少的限制

## Git软件，分布式版本控制系统
  仓库管理软件，使用git管理私人代码和企业代码

     本地内容                         发布内容
  version1.1（新版）--Git(更新)--> version 1.0(旧版)

## 设备认证
1. 让网站的账户与设备绑定，后续完成代码的管理，上传下载
   
   git init  //创建本地仓库  *后续对仓库的操作都要在仓库位置（master）*
   
   git config --list  //查看git的配置文件
  
   修改或添加config配置项：
   
   git config --global user.email ”我的邮箱“ //注册邮箱
   
   git config --global user,name "用户名"    //注册用户名

   创建本地密文：

   ssh-keygen -t rsa -C "注册邮箱"  //创建本地密文
                                

   (-t 加密类型 )           出现图标（->找密文串），创建成功！

   //去对应目录下找密文文件(rsa.pub)复制此密文，（若无邮箱，则失败）

   //关联: github-> setting-> SSH key and GPG-> new ssh key 测试密钥->粘贴

   //测试关联是否完成：
    ssh -T git@github.com            //ssh远程登陆  yes--Hi

2. 为目标仓库起别名，定位目标仓库，后续上传
   git remote add orgin "ssh地址（云端地址）"  //为ssh仓库地址创建别名为orgin
  
               //操作地址      //粘贴的仓库地址

   git remote remove origin       //删除origin别名


## 本地仓库与云端仓库的交互逻辑
![本地仓库与云端仓库的交互逻辑](C:/Users/DELL//Desktop//2.png)
 
git add code.c    //添加内容

将缓冲区数据提交到本地仓库：

git commit     //提交到本地仓库

git commit -m "备注信息”  //生成提交记录

git push origin（云端仓库地址） master    //将本地仓库内容推到云端仓库

git status      //查看状态

git rm code.c   //删除本地文件及仓库数据

git restore code.c  //复位删除文件（前提：仓库存在）


## 代码更新的依赖关系被破坏
本地内容要比云端新，完成更新替换，但若直接修改云端内容，导致本地内容无法再次提交

解决方法：

**先拉取git pull云端内容，与本地内容合并或操作，而后再次推即可。**

git pull --rebase origin master

git rebase --abort  //忽略新版，此时不能上传
 
git rebase --skip   //需略旧版，更新本地后可以上传（忽略本地内容，保留云端内容）

git rebase --continue //版本合并，解决冲突后可以直接上


## 下载开源代码
git clone "HTTPS仓库地址"   //下载开源项目code资源






---
---

# MarkDown语言

MarkDown,文本修饰语言，用特殊符号修饰正文效果<br>


## 标题修饰符\#

# 标题修饰符（一级标题）
## （二级标题）
### （三级标题）
#### （四级标题）
##### （五级标题）



## 正文内容
  
  输入正文内容 ，但是如果需要换行，用\<br\>标签


## 修饰正文
  
  *一段测试文本*

  **一段测试文本**
  
  ***一段测试文本***
  
  ~~一段测试文本~~     表示删除

  这是一段测试文本，将`关键字`。重点显示


## 分割线

   用\-\-\-表示分割线 

---



## 引用效果用\>表示

>一级引用 
>>二级引用
>>>三级引用



## 列表修饰符（后都有空格）

### 无序列表\*
* 二次元游戏
  * 元神
    * 神
* 大逃杀
  * PUBG
  * APEX

### 有序列表 1.
1. 物理学
   1. 粒子物理
   2. 原子核物理
   3. 凝聚态物理
2. 计算机科学
   1. 分布式架构
   2. 云计算


### 混合列表（有序+无序）
1. 测试一级
   * 测试二级
    2. 测试三级 


### 表格
名称|技能|排行
--|:--:|--:  
蝙蝠|有钱|32
海王|游泳|16
闪电侠|跑|10

###代码片段

```c
   	#include<stdio.h>
```
```cpp
	#include<iostream>
```
```python
       import <os>
```
```bash
```



### 超链接技术 

[Github](https://www.github.com "点击访问")


### 插入图片

![壁纸截图](C://Users//DELL//Desktop//1.jpg "悬停标题")



