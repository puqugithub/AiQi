AiQi
==========
AiQi是一款人工智能软件，它支持形式化地从中文中去提取语句记忆和命题逻辑推理，你也可以加载程序目录自带的聊天语料文件，让AiQi变身聊天娱乐机器人！

AiQi拥有一个可视化的记忆单元编辑平台BrainBox，每一个AiQi记忆中的概念都可以在这个平台里编辑和修改。

AiQi 使用指南
-------------
◎>>让AiQi记住简单的主谓宾关系语句
语句格式1：[名词][动词][名词]
例子：我想你
语句格式2：[名词][是][名词]
例子：我是人类


◎>>强制让AiQi记住一个概念
语句格式1：记住[名词]
例子：记住太阳
语句格式2：记住[复合名词]
例子：记住[小明的爸爸]


◎>>强制让AiQi记住一个命题
语句格式2：记住[名词][动词][名词]
例子：记住熊猫吃竹子


◎>>强制让AiQi记住一个带属性标签的记忆
语句格式2：记住[名词][标签]XXXX
例子：记住小明名字是某某某
例子：记住苹果颜色为红色
标签文件CK/SXBQ.txt，标签内容用户可添加


◎>>让AiQi把两个概念建立起条件反射关系
语句格式1：如果xxx那么YYY
语句格式2：如果[词语]那么[词语]
语句格式3：如果[句子]那么[句子]
例子：如果下雨那么带伞


◎>>让AiQi对一个概念（命题）进行逻辑（真/假）判断
语句格式1：[名词]? 
语句格式2：[名词][动词][名词]吗
语句格式3：[名词]是不是[动词][名词]


◎>>让AiQi对提问作出回答,提问的前提是概念必须存在，可以是任意动词的命题提问
语句格式1：[名词][动词]什么?
语句格式2：什么[动词][名词]
语句格式3：[名词]什么


◎>>对AiQi的回答作出评价，奖励或者惩罚AiQi
（只有AiQi回答用户输入后开启，并在一段有效时间内输入才有效，这是一个简单的回答评价机制）
语句格式：当AiQi回答后，用户输入 “是、是的、对、yes；不、不对、错、no”等关键字
语句作用: 用户对AiQi当前回答做出评价，评价具有对记忆数据的奖励、和惩罚功能！


◎>>网上查询天气
语句格式：[地区]天气
例子：上海天气


◎>>网上查询词条
语句格式1：[名词]是什么
例子：哲学是什么
语句格式2：什么是[名词]
例子：什么是宇宙
注：如果一个概念曾经灌输过“是什么”的记忆，那么回答记忆内容


### 条件反射的例子：
使用"如果...那么..."的格式语句，可以建立概念与概念之间的反射联系
1. 请输入例句：如果灯亮了那么有食物
2. 请再次输入：如果有食物那么流口水
3. 查看结果，输入：灯亮了
4. 请打开记忆编辑器，大家会看到刚才输入的内容，反射链已经建立，并且反射链的单元全部激活了！

以后只要激活“灯亮了”都会间接激活流口水了！
这是个经典例子，内容格式可以在"如果...那么..."的语句中任意变化，并且反复输入将会强化反射联系

### 逻辑推理的例子：
>我：   盼盼是熊猫
>爱奇： 哦，记住了。
>我：   熊猫吃竹子
>爱奇： 哦，记住了。
>我：   盼盼吃竹子吗?
>爱奇： 是，我觉得盼盼吃竹子
>我：   盼盼不吃竹子吗
>爱奇： 不，我觉得盼盼吃竹子
>我：   盼盼吃什么
>爱奇： 我觉得盼盼吃竹子


>我：   记住苏格拉底是人
>爱奇： 哦，记住了。
>我：   人会死
>爱奇： 哦，记住了。
>我：   苏格拉底会死吗?
>爱奇： 是，我认为苏格拉底会死


一个简单的真值逻辑推理,我没有直接告诉AI,"苏格拉底会死"，而我只告诉AI"人会死"，有告诉AI"苏格拉底是人"，
AI会逻辑推理出"苏格拉底"也有死的属性，完成了三段论推理。（以上都是即时输入的结果，是AiQi最经典的逻辑推理例子）



### 联网自动学习
点击“自动学习”按钮，AiQi将会自动联网进行词条概念学习，学习的内容就是记忆中已有的概念，当然你也可以为AiQi增加记忆中概念的数量，AiQi会学得更多。
在输入框中输入任意字符可以停止自动学习


### 脚本命令
用户可以在某个概念的数据中加入脚本命令，当该条数据激活后。系统将执行该条数据中的脚本代码，完成用户预编的命令处理

数据前要用标签<脚本命令>，来标示这条数据是脚本数据。
脚本命令之间必须用";"分割，目前只支持三种脚本命令（输出文字、打开网站、查询天气），如以下格式：


用户可以在某个概念的数据条中加入：
例1：
<脚本命令>打开网站(www.baidu.com);输出文字(主人，我帮您打开了百度网站);

例2：
<脚本命令>查询天气(上海);


### 系统命令
以@开头做标示，完成对AI系统操作的文字命令，可在普通输入中使用

1. 查看概念中的数据信息
>格式：@查看概念 概念名
>例子：@查看概念 人类

2. 删除概念
>格式：@删除概念 概念名
>例子：@删除概念 苹果

3. 删除概念中的数据
>格式：@删除概念数据 概念名(数据ID)
>例子：@删除概念数据 苹果(1)

4. 对语句进行分词测试
>格式：@分词 语句
>例子：@分词 今天天气真好啊！

5. 网上学习
>格式：@网上学习 词条
>例子：@网上学习 咖啡

6. 打开网页
>格式：@网页 网址
>例子：@网页 www.baidu.com

7. 天气查询
>格式：@天气 地区/省份名称
>例子：@天气 上海


### 数据标签说明：
AiQi记忆中每个概念都有成员数据，带标签的数据是知识数据，不带标签的是普通数据。

标签说明：
<是>          一种单向反射关系，激活传递关系
<不是>        一种单向反射关系，抑制作用关系
<动词>        行为标签
<因果>        如果...那么...建立的数据
<内容>        可用于输入匹配的数据
<脚本命令>    可执行的脚本命令语句
自定义标签    保存在CK/SXBQ.txt中，用户自定义标签，用于识别