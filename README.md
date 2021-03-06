
# Contributions-Pen
![](https://img.shields.io/badge/PHP-%5E7.0.0-blue.svg 'img')   ![](https://img.shields.io/badge/OS-Windows%20%7C%20Linux%20%7C%20Mac%20OS%20X-green.svg 'img')  
Draw in GitHub contributions graph
![](https://github.com/Kurisu-A/Contributions-Pen/blob/master/img/kurisu2.png)
> 更多样例预览点击 [link](https://github.com/Kurisu-A/Contributions-Pen#show)

## 简介
利用 `PHP` 脚本,在 `GitHub` 的 提交日历上绘制图案

**该脚本可能会破坏你的提交日历, 请谨慎使用**

> 虽然其实已经有很多相同的轮子了。。比如greenHat，比如gitfiti，但是greenHat没有办法让我画画。。。gitfiti的话开始造轮子的时候还不是太熟PY，导致有些硌手。。。。。。所以无奈。。自己用php造了个轮子。。。

## 运行环境
推荐 `PHP7以上` , `Windows`/`Linux`/`Mac OS X` 操作系统皆可

**请确认 `PHP` 已经添加到环境变量中**

## 原理
利用将 `某次提交` 指定日期重复提交, 达到在 `GitHub 提交日历` 上进行绘画的效果

## 使用方法
1. 运行 `git clone https://github.com/Kurisu-A/Contributions-Pen.git` 将脚本拉取到本地文件夹 `A`
2. 在 `GitHub` 新建一个储存库, 名称自定义 
3. 将新建的空的储存库使用 `git clone ********` 拉取到本地 `B`
4. 将刚刚第一次拉取的 `A` 文件夹中的 `draw.php` 和 `config.php` 放入文件夹 `B` 中
5. 在文件夹 `B` 中运行指令 `php draw.php` 

> 运行时间视图案的复杂程度而定，复杂一些的图案会在^10min中完成
>
> 出现问题欢迎在 issue 中交流

## 可以修改的配置
通过调整 `config.php` 文件中的配置, 提供一定的变化

> **autoCenter**
>
> 如果设为 `true` ,则自动居中
>
> **beginningBlank**
>
> 如果设为`n`, 则在开头空出 `n`列
>
> **user.name (必填)**
>
> 进行本次提交的用户名
>
> **user.email (必填 **
>
> 进行本次提交的邮箱 **请注意保护隐私**
> [learn more about this](https://help.github.com/articles/why-are-my-contributions-not-showing-up-on-my-profile/)
>

**通过调整 `draw.php` 文件来得到的变化**

> 调整 arr中的排列,来改变绘制的图案,使用 `X` 字符, 或者别的字符 `([a-zA-Z])` 来标识一次提交, 使用数字来表示多次提交 `(/\d{0,9}/)`,使用配置中配置的 `_` 来表示不提交`(可以在配置中修改)`
>
```PHP
<?php
$arr = [
      '_ _ _ 3 _ _ 3 _ _ ',
      '_ _ 3 3 3 3 3 3 _ ',
      '_ _ 3 3 3 3 3 3 _ ',
      '_ _ 3 3 3 3 3 3 _ ',
      '_ 3 _ _ 3 3 _ _ _ ',
      '_ _ 3 3 3 3 3 _ _ ',
      '_ _ _ _ 3 3 3 _ _ ',
  ];
```
>
------
## show
![](https://github.com/Kurisu-A/Contributions-Pen/blob/master/img/github.png)
![](https://github.com/Kurisu-A/Contributions-Pen/blob/master/img/life%20is%20short.png)
![](https://github.com/Kurisu-A/Contributions-Pen/blob/master/img/php_is_best.png)
![](https://github.com/Kurisu-A/Contributions-Pen/blob/master/img/go_is_best.png)
![](https://github.com/Kurisu-A/Contributions-Pen/blob/master/img/talk_is_cheap.png)

## 建议
在运行代码之前，可以使用 `img/basic.png` 的基础图，在 Photoshop 中先画出效果图，然后再在代码中编辑字符串，减少尝试的次数  
![](https://github.com/Kurisu-A/Contributions-Pen/blob/master/img/basic.png)

## 同类项目
[angusshire/greenhat](https://github.com/angusshire/greenhat)
> 用绿色覆盖整个提交日历

[gelstudios/gitfiti](https://github.com/gelstudios/gitfiti)
> Python实现在提交日历上绘制图案

## LICENSE
* MIT
