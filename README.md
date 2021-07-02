---
layout: page
title: "Github markdown"
author: 果冻虾仁
permalink: /help/dns/
编号: 
    - 0001
    - "2222"
---

Gigthub markdown语法
==


该文件用来测试和展示书写README的各种markdown语法。  
GitHub的markdown语法在标准的markdown语法基础上做了扩充，  
称之为`GitHub Flavored Markdown`，简称`GFM`。GFM在GitHub上有广泛应用，  
除了README文件外，issues和wiki均支持markdown语法。

****
	
Author |果冻虾仁
--- |---
E-mail |Jelly.K.Wang@qq.com


****
## 目录
* [规范](#规范)
* [横线](#横线)
* [标题](#标题)
* [文本](#文本)
    * 普通文本
    * 单行文本
    * 多行文本
    * 换行
    * 文字高亮
    * 斜体
    * 粗体
    * 删除线
* [图片](#图片)
    * 来源于网络的图片
    * GitHub仓库中的图片
* [链接](#链接) 
    * 文字超链接
        *  链接外部URL
        *  链接本仓库里的URL
    *  锚点
    * [图片链接](#图片链接)
    * Reference索引超链
    * 自动链接
* [列表](#列表)
    * 无序列表
    * 有序列表
    * 复选框列表
* [块引用](#块引用)
* [代码高亮](#代码高亮)
* [表格](#表格) 
* [表情](#表情)
* [diff语法](#diff语法)
* [details折叠语法](#details折叠语法)
* [注释](#注释)
* [其他](#其他)
    * github markdown暂不支持功能
    * 上标
    * 下标
    * 自定义锚点
    * 参考资料注解

规范
--

### 文件后缀
建议使用.md

### 字符集
建议使用UTF-8

### 换行符
建议使用LF，unix系统风格的换行符

### 默认规定
* README.md文件会被 github、gitlab等版本控制系统自动展示

横线
--
```text

***

---

___

```
都表示横线，效果是一样的，可以写把*、-、_ 重复三次以上，与其他内容前后都空一行，避免产生其他问题

***

---

___


标题
--

```text
# 一级标题  
## 二级标题  
### 三级标题  
#### 四级标题  
##### 五级标题  
###### 六级标题  
```

# 一级标题  
## 二级标题  
### 三级标题  
#### 四级标题  
##### 五级标题  
###### 六级标题  

* 一级标题--Setex风格

下面的= 个数 >= 1，建议都写2个
```text
一级标题--Setex风格
```

一级标题--Setex风格
==

```text
一级标题--Setex风格
==

等价于

# 一级标题--Setex风格
```
前一种写法一般用于文件的第一行写大标题


* 二级标题--Setex风格

下面的- 个数 >= 1，建议都写2个
```text
二级标题--Setex风格
--
```

二级标题--Setex风格
--

```text
二级标题--Setex风格
--

特价于

## 二级标题--Setex风格
```


文本
--

### 普通文本
这是一段普通的文本，直接写，开头顶格

### 单行文本
    Hello,大家好，我是果冻虾仁。
在一行开头加入1个Tab或者4个空格。

### 文本块
#### 语法1
在连续几行的文本开头加入1个Tab或者4个空格。

    欢迎到访
    很高兴见到您
    祝您，早上好，中午好，下午好，晚安

#### 语法2
文本首、尾各3个反引号：
```
欢迎到访
我是C++码农
你可以在知乎、CSDN、简书搜索【果冻虾仁】找到我
```
该语法也可以实现代码高亮，见[代码高亮](#代码高亮)

#### 换行
直接回车不能换行  
* 可以在上一行文本后面加两个空格，  
这样下一行的文本就换行了。

* 或者在两行之间加一个空行，

也能实现换行效果，不过这个行间距有点大。

#### 文字高亮
文字高亮功能能使行内部分文字高亮，使用一对反引号，还可以避免转义  
* 语法
```
`linux` `网络编程` `socket` `epoll` 
```
效果：`linux` `网络编程` `socket` `epoll`

也适合做一篇文章的tag

#### 斜体、粗体、删除线
|语法 |效果 |
|--- |--- |
|`*斜体1*` |*斜体1* |
|`_斜体2_` | _斜体2_ |
|`**粗体1**` |**粗体1** |
|`__粗体2__` |__粗体2__ |
|`这是一个 ~~删除线~~` |这是一个 ~~删除线~~ |
|`***斜粗体1***` |***斜粗体1*** |
|`___斜粗体2___` |___斜粗体2___ |
|`***~~斜粗体删除线1~~***` |***~~斜粗体删除线1~~*** |
|`~~***斜粗体删除线2***~~` |~~***斜粗体删除线2***~~ |
|`___~~斜粗体删除线3~~___` |___~~斜粗体删除线3~~___ |
|`~~___斜粗体删除线4___~~` |~~___斜粗体删除线4___~~ |

    斜体、粗体、删除线可混合使用

图片
--
基本格式：
```
![alt](URL "title")
```
alt和title即对应HTML中的alt和title属性（都可省略）：
- alt表示图片显示失败时的替换文本
- title表示鼠标悬停在图片时的显示文本（注意这里要加引号）

URL即图片的url地址，如果引用本仓库中的图片，直接使用**相对路径**就可了，  
如果引用其他github仓库中的图片要注意格式，即：`仓库地址/raw/分支名/图片路径`，如：
```
https://github.com/guodongxiaren/ImageCache/raw/master/Logo/foryou.gif
```

|# |语法 |效果 |
|--- |--- |--- |
|1 |`![baidu](http://www.baidu.com/img/bdlogo.gif "百度logo")` |![baidu](http://www.baidu.com/img/bdlogo.gif "百度logo") |
|2 |`![][code-past]` |![][code-past] |

注意例2的写法使用了**URL变量**的形式，在[链接](#链接)一节有介绍。
>在文末有code-past的定义：
```
[code-past]:https://img-blog.csdnimg.cn/201908060004034.png
```

链接
--
### 链接外部URL

|# |语法 |效果 |
|--- |--- |--- |
|1 |`[我的博客](http://blog.csdn.net/guodongxiaren "悬停显示")` |[我的博客](http://blog.csdn.net/guodongxiaren "悬停显示") |
|2 |`[我的知乎][zhihu] ` |[我的知乎][zhihu] |

引用链接由两个[]组成：
```text
* 非图片链接
[链接文本][URL变量]

* 图片链接
![alt][URL变量]
```
- 第二个[]为实际的URL

>使用URL变量能达到复用的目的，一般把全文所有的URL标识符统一放在文章末尾，这样看起来比较干净。


### 链接本仓库里的URL

|语法 |效果 |
|--- |--- |
|`[我的简介](/example/profile.md)`|[我的简介](/example/profile.md) |
|`[example](./example)` |[example](./example) |

### 图片链接
给图片加链接的本质是混合图片显示语法和普通的链接语法。普通的链接中[ ]内部是链接要显示的文本，而图片链接[ ]里面则是要显示的图片。  
直接混合两种语法当然可以，但是十分啰嗦，为此我们可以使用URL标识符的形式。

|# |语法 |效果 |
|--- |--- |:---: |
|1 |`[![weibo-logo]](http://weibo.com/linpiaochen)` |[![weibo-logo]](http://weibo.com/linpiaochen) |
|2 |`[![](/img/zhihu.png "我的知乎，欢迎关注")][zhihu]` |[![](/img/zhihu.png "我的知乎，欢迎关注")][zhihu] |
|3 |`[![csdn-logo]][csdn]`|[![csdn-logo]][csdn] |

因为图片本身和链接本身都支持URL标识符的形式，所以图片链接也可以很简洁（见例3）。  
注意，此时鼠标悬停时显示的文字是图片的title，而非链接本身的title了。
>本文URL变量都放置于文末

### 锚点
每一个标题都是一个锚点，和HTML的锚点（`#`）类似
* 锚点标记中含特殊符时，在链接中把特殊符去掉即可
* 如果有空格使用`-`代替
* `-` 可以用`\-`转义

|语法 |效果 |
|--- |--- |
|`[回到顶部](#readme)` |[回到顶部](#readme) |

不过要注意，标题中的英文字母都被转化为**小写字母**了。
> 以前GitHub对中文支持的不好，所以中文标题不能正确识别为锚点，但是现在已经没问题啦！

### Reference索引链接
即引用链接

```text
[百度][b]  
[b]:https://www.baidu.com
```
[b]:https://www.baidu.com 定义URL变量[b]，不会显示

**效果**  
[百度][b]  
[b]:https://www.baidu.com

### 自动链接
尖括号
```text
<http://ibruce.info>  
<bu.ru@qq.com>
```
<http://ibruce.info>  
<bu.ru@qq.com>

### 嵌入视频
使用html中的video标签，github markdown暂不支持，Typora支持
```html
<video class="player" 
    src="media/realEstateAD.mp4" 
    poster="https://p9-dy.byteimg.com/img/tos-cn-p-0015/7bb4669a00c7480889e0023ddd59c875_1585735351~c5_300x400.jpeg?from=2563711402_large"
    type="video/mp4" 
    preload="auto" 
    controls="controls" 
    style="width: 100%;"
    >

</video>
```

```text
src: 指定视频资源的URL
poster: 视频预览图片
type: 视频文件类型
preload: 是否预加载，auto：自动预加载，none: 不预加载
```

<video class="player" 
    src="media/realEstateAD.mp4" 
    poster="https://p9-dy.byteimg.com/img/tos-cn-p-0015/7bb4669a00c7480889e0023ddd59c875_1585735351~c5_300x400.jpeg?from=2563711402_large"
    type="video/mp4" 
    preload="auto" 
    controls="controls" 
    style="width: 100%;"
    >
</video>

### 嵌入音频
使用html中的audio标签，github markdown暂不支持，Typora支持
```html
<audio controls="" preload="auto" height="0" width="0" autoplay="false"
       src="http://119.147.228.28/amobile.music.tc.qq.com/C400001R8Zeo1tf1fS.m4a?guid=3070280983&amp;vkey=D73F717249D433A37DF1E10D13FC530839A5C96FEF39B46B40CA4F50EF784ABB9D7CD5DDA90A668847F1E0FAAFC3AA3060B043C62B22B2E4&amp;uin=7078&amp;fromtag=66"
       >
    <source id="mp3" 
        src="http://119.147.228.28/amobile.music.tc.qq.com/C400001R8Zeo1tf1fS.m4a?guid=3070280983&amp;vkey=D73F717249D433A37DF1E10D13FC530839A5C96FEF39B46B40CA4F50EF784ABB9D7CD5DDA90A668847F1E0FAAFC3AA3060B043C62B22B2E4&amp;uin=7078&amp;fromtag=66"
    >
</audio>
```

```text
preload: 是否预加载
audio标签src属性：预加载音频资源的URL路径
source标签中的src属性：指定音频资源URL，需要与audio标签src属性性相同
```

<audio controls="" preload="auto" height="0" width="0" autoplay="false"
       src="http://119.147.228.28/amobile.music.tc.qq.com/C400001R8Zeo1tf1fS.m4a?guid=3070280983&amp;vkey=D73F717249D433A37DF1E10D13FC530839A5C96FEF39B46B40CA4F50EF784ABB9D7CD5DDA90A668847F1E0FAAFC3AA3060B043C62B22B2E4&amp;uin=7078&amp;fromtag=66"
       >
    <source id="mp3" 
        src="http://119.147.228.28/amobile.music.tc.qq.com/C400001R8Zeo1tf1fS.m4a?guid=3070280983&amp;vkey=D73F717249D433A37DF1E10D13FC530839A5C96FEF39B46B40CA4F50EF784ABB9D7CD5DDA90A668847F1E0FAAFC3AA3060B043C62B22B2E4&amp;uin=7078&amp;fromtag=66"
    >
</audio>


列表
--
### 无序列表
* 语法  
无序列表符: * - +
```
* 昵称：果冻虾仁
- 别名：隔壁老王
+ 英文名：Jelly
```
**效果**  
* 昵称：果冻虾仁
- 别名：隔壁老王
+ 英文名：Jelly

### 多级无序列表
* 语法
```
* 编程语言
    ```text
    这时开发效率最高的语言
    ...
    ```
    * 脚本语言
        * Python
```
**效果**  
* 编程语言
    ```text
    这时开发效率最高的语言
    ...
    ```
    * 脚本语言
        * Python

### 一级有序列表
* 语法
    ```text
    就是在数字后面加一个点，再加一个空格。  
    序号可以全部写一个，如1，让其自动推断
    ```
     
```
面向对象的三个基本特征：

1. 封装
2. 继承
3. 多态
```

**效果**  
面向对象的三个基本特征：

1. 封装
2. 继承
3. 多态

**序号自行推断示例**  
```text
1. 封装
1. 继承
1. 多态
```
1. 封装
1. 继承
1. 多态

### 多级有序列表
和无序列表一样，有序列表也有多级结构。
* 语法
```
1. 这是一级的有序列表，数字1还是1
   1. 这是二级的有序列表，阿拉伯数字在显示的时候变成了罗马数字
      1. 这是三级的有序列表，数字在显示的时候变成了英文字母
```

**效果**
1. 这是一级的有序列表，数字1还是1
   1. 这是二级的有序列表，阿拉伯数字在显示的时候变成了罗马数字
      1. 这是三级的有序列表，数字在显示的时候变成了英文字母
	 

### 复选框列表
* 语法
```text
- [ ] content 
-空格[空格]空格content 

解释: [ ]括号里面的空格可以换成[x],代表选中对话框
```

* 示例  
```
- [x] 需求分析
- [x] 系统设计
- [x] 详细设计
- [ ] 编码
- [ ] 测试
- [ ] 交付
```

**效果**  
- [x] 需求分析
- [x] 系统设计
- [x] 详细设计
- [ ] 编码
- [ ] 测试
- [ ] 交付

您可以使用这个功能来标注某个项目各项任务的完成情况。
> Tip:
>> 在GitHub的**issue**中使用该语法是可以实时点击复选框来勾选或解除勾选的，而无需修改issue原文。


块引用
--

### 常用于引用文本

* 块引用示例
```text
文本摘自《深入理解计算机系统》P27  
令人吃惊的是，在哪种字节顺序是合适的这个问题上，人们表现得非常情绪化。
实际上术语“little endian”（小端）和“big endian”（大端）出自Jonathan Swift的
《格利佛游记》一书，其中交战的两个派别无法就应该从哪一端打开一个半熟的鸡蛋达成一致。
因此，争论沦为关于社会政治的争论。只要选择了一种规则并且始终如一的坚持，
其实对于哪种字节排序的选择都是任意的。
```
>**“端”（endian）的起源**  
以下是Jonathan Swift在1726年关于大小端之争历史的描述：  
“……下面我要告诉你的是，Lilliput和Blefuscu这两大强国在过去36个月里一直在苦战。战争开始是由于以下的原因：我们大家都认为，吃鸡蛋前，原始的方法是打破鸡蛋较大的一端，可是当今的皇帝的祖父小时候吃鸡蛋，一次按古法打鸡蛋时碰巧将一个手指弄破了，因此他的父亲，当时的皇帝，就下了一道敕令，命令全体臣民吃鸡蛋时打破较小的一端，违令者重罚。”

### 块引用有多级结构
* 语法
```
> 数据结构
>> 树
>>> 二叉树
>>>> 平衡二叉树
>>>>> 满二叉树
```
**效果**  
> 数据结构
>> 树
>>> 二叉树
>>>> 平衡二叉树
>>>>> 满二叉树


代码高亮
--

* 代码高亮语法

在三个反引号后面加上编程语言的名字，另起一行开始写代码，最后一行再加上三个反引号。

    ```java
    public static void main(String[]args){} //Java
    ```
    
    ```c
    int main(int argc, char *argv[]) //C
    ```
    
    ```bash
    echo "hello GitHub" #Bash
    ```
    
    ```javascript
    document.getElementById("myH1").innerHTML="Welcome to my Homepage"; //javascipt
    &#96;&#96;&#96;
    
    ```cpp
    string &operator+(const string& A,const string& B) //cpp
    ```

**代码高亮效果**  
```java
public static void main(String[]args){} //Java
```

```c
int main(int argc, char *argv[]) //C
```

```bash
echo "hello GitHub" #Bash
```

```javascript
document.getElementById("myH1").innerHTML="Welcome to my Homepage"; //javascipt
```

```cpp
string &operator+(const string& A,const string& B) //cpp
```

表格
--
注意：表头上面一行为文本块时，需要在文本块与表头之间空一行

```text
|表头1 |表头2 |
|--- |--- |
|表格单元 |表格单元 |
|表格单元 |表格单元 |
```

|表头1 |表头2 |
|--- |--- |
|表格单元 |表格单元 |
|表格单元 |表格单元 |


```text
表头1 |表头2
--- |---
表格单元 |表格单元
表格单元 |表格单元
```
表头1 |表头2
--- |---
表格单元 |表格单元
表格单元 |表格单元

### 表格对齐
表格可以指定对齐方式

```text
左对齐 |居中  |右对齐
:--- |:---: |---: 
col 3 is      |some wordy text |$1600
col 2 is      |centered        |$12
zebra stripes |are neat        |$1
坚线特殊符    |在表格中使用\转换无效 <br>需使用Unicode编码`&#124;`        |&#124;
```

左对齐 |居中  | 右对齐
:--- |:---: |---: 
col 3 is      |some wordy text |$1600
col 2 is      |centered        |$12
zebra stripes |are neat        |$1
坚线特殊符    |在表格中使用\转换无效 <br>需使用Unicode编码`&#124;`        |&#124;


### yaml风格表格
必须写在文件的首行，见本文最上方  

    ---
    layout: page
    title: "Github markdown"
    author: 果冻虾仁
    permalink: /help/dns/
    编号: 
        - 0001
        - "2222"
    ---


### 混合其他语法
表格单元中的内容可以和其他大多数GFM语法配合使用

#### 使用普通文本的删除线，斜体等效果

|名字 |描述 |
|--- |--- |
|Help      | ~~Display the~~ help window.|
|Close     |_Closes_ a window     |

#### 表格中嵌入图片（链接）
其实前面介绍图片显示、图片链接的时候为了清晰就是放在在表格中显示的。

|图片 |描述 |
|--- |--- |
|![baidu][baidu-logo] |百度 |

表情
--
Github的Markdown语法支持添加emoji表情，输入不同的符号码（两个冒号包围的字符）可以显示出不同的表情。

比如`:blush:`，可以显示:blush:。

具体每一个表情的符号码，可以查询GitHub的官方网页[http://www.emoji-cheat-sheet.com](http://www.emoji-cheat-sheet.com)。

但是这个网页每次都打开**奇慢**。所以我整理到了本repo中，大家可以直接在此查看[emoji 表情](./emoji.md)。

diff语法
--
版本控制的系统中都少不了diff的功能，即展示一个文件内容的增加与删除。  
GFM中可以显示的展示diff效果。使用绿色表示新增，红色表示删除。

* 语法
    ```text
    其语法与代码高亮类似，指定语言类型为diff
    + : 新增 (绿)
    - : 删除 (红)
    ! : 修改 (橙)
    # : 未变动 (灰)
    ```

* diff示例  
    ![](./img/diff.png)  

**效果**  
```diff
+ 人闲桂花落，
- 夜静春山空。
! 月出惊山鸟，
# 时鸣春涧中。
```

details折叠语法
--
* `</summary>` 与下面的内容之间一定要空一行
* `</details>` 与下面的内容之间一定要空一行，否则影响下面的内容格式

```text
<details>
<summary>射雕英雄传</summary>

1. 第一回 风雪惊变
1. 第二回 江南七怪
1. 第三回 黄沙莽莽
1. 第四回 黑风双煞
1. 第五回 弯弓射雕
1. 第六回 崖顶疑阵
1. 第七回 比武招亲
</details>
```

<details>
<summary>射雕英雄传</summary>

1. 第一回 风雪惊变
1. 第二回 江南七怪
1. 第三回 黄沙莽莽
1. 第四回 黑风双煞
1. 第五回 弯弓射雕
1. 第六回 崖顶疑阵
1. 第七回 比武招亲
</details>

注释
--
* html块注释
    ```text
    <!--
    哈哈我是注释，
    不会在浏览器中显示。
    -->
    ```
<!--
哈哈我是注释，
不会在浏览器中显示。
-->

* 行注释
    ```text
    [//]:#(注释内容...)
    ```

[//]:#(注释内容...)

其他
--
### github markdown暂不支持的功能
* 目前github暂时不支持markdown流程控制语法
* 目前github暂时不支持css语法，如字体颜色、字体等
* 目前github不支持文本块行号显示
* [嵌入视频](#嵌入视频)
* [嵌入音频](#嵌入音频)

### 上标
```text
2<sup>3</sub>
```
**效果**  
2<sup>3</sub>

### 下标
```text
H<sub>2</sub>O
```
**效果**  
H<sub>2</sub>O

### 自定义锚点
```text
解析器会为标题分配一个锚点id。
但有时候需要连接到不是标题的区域中
这时用自定义锚点方法，再合适不过了
```
1. 标记要跳转到的位置
    ```text
    <span id="myjump">提示信息</span>
    如果不想显示 提示信息，可以什么都不写
    如：
    <span id="myjump"></span>
    ```
2. 在需要连接到锚点的地方使用锚点
    ```text
    [说明文字](#myjump)
    ```

### 参考资料注解
百科文章里，有些文字后有 <sup>[\[1\]]</sup>，表示参考资料引用，点击可跳转过去  
这里可以用 自定义锚点 + 上标 方法来做

```text
百科文章里，有些文字后有 <sup>[\[1\]]</sup>，表示参考资料引用，点击可跳转过去  
这里可以用 自定义锚点 + 上标 方法来做

[\[1\]]:https://baike.baidu.com/ "百度百科"
```

--------------------------------
<!--
定义URL变量(URL标识)，方便上文引用

* 语法
[URL变量名]:URL地址

变量名：支持数字、字母、-、_、中文的组合


* 引用方法
    * 非图片
[链接文本][已定义的URL变量]    
    * 图片
![alt][已定义的URL变量]

定义位置：可以是文档的任意位置，建议放在文末

* 定义的URL变量展示时不显示
-->
[csdn]:http://blog.csdn.net/guodongxiaren "我的博客"
[zhihu]:https://www.zhihu.com/people/jellywong "我的知乎，欢迎关注"
[weibo]:http://weibo.com/linpiaochen
[baidu-logo]:http://www.baidu.com/img/bdlogo.gif "百度logo"
[weibo-logo]:/img/weibo.png "点击图片进入我的微博"
[csdn-logo]:/img/csdn.png "我的CSDN博客"
[code-past]:https://img-blog.csdnimg.cn/201908060004034.png
[\[1\]]:https://baike.baidu.com/ "百度百科"

```text
// 定义URL变量
[csdn]:http://blog.csdn.net/guodongxiaren "我的博客"
[zhihu]:https://www.zhihu.com/people/jellywong "我的知乎，欢迎关注"
[weibo]:http://weibo.com/linpiaochen
[baidu-logo]:http://www.baidu.com/img/bdlogo.gif "百度logo"
[weibo-logo]:/img/weibo.png "点击图片进入我的微博"
[csdn-logo]:/img/csdn.png "我的CSDN博客"
[code-past]:https://img-blog.csdnimg.cn/201908060004034.png
[\[1\]]:https://baike.baidu.com/ "百度百科"
```
