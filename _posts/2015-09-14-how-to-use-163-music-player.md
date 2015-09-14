---
layout: post
title: 在markdown日志中使用网易云音乐外链播放器
excerpt: "如题，顺便扯扯淡"
modified: 2015/09/15 1:19:06  
tags: [markdown,iframe]
comments: true
image:
  feature: pixabay/concert.jpg
  credit: Pixabay
  creditlink: https://pixabay.com/zh/%E9%9F%B3%E4%B9%90%E4%BC%9A-%E4%BA%BA%E7%BE%A4-%E8%A7%82%E4%BC%97-%E4%BA%BA-%E9%9F%B3%E4%B9%90-%E5%A8%B1%E4%B9%90-%E8%8A%82%E6%97%A5-%E6%80%A7%E8%83%BD-%E4%B9%90%E8%B6%A3-%E4%B9%90%E9%98%9F-768722/
---

## 先来首歌吧：

<iframe frameborder="no" border="0" marginwidth="0" marginheight="0" width="330" height="86" src="http://music.163.com/outchain/player?type=2&id=29535531&auto=0&height=66"></iframe>

来自陈粒的《历历万乡》，原名叫《七月洪流》。歌词太美，词作者陈南西据说是陈粒的高中同学，毕业于清华大学法学院。“她尝遍了每个异乡限时赠送的糖”和“你扔下的习惯还顽强活在我身上”简直了，这两句实在佩服。

	作曲 : 陈粒
    作词 : 陈南西

    她住在七月的洪流上
    天台倾倒理想一万丈
    她午睡在北风仓皇途经的芦苇荡
    她梦中的草原白茫茫
    列车搭上悲欢去辗转
    她尝遍了每个异乡限时赠送的糖

    如果我站在朝阳上 能否脱去昨日的惆怅
    单薄语言能否传达我所有的牵挂
    若有天我不复勇往 能否坚持走完这一场
    踏遍万水千山总有一地故乡

    城市慷慨亮整夜光
    如同少年不惧岁月长
    她想要的不多只是和别人的不一样
    烛光倒影为我添茶
    相逢太短不等茶水凉
    你扔下的习惯还顽强活在我身上

    如果我站在朝阳上 能否脱去昨日的惆怅
    单薄语言能否传达我所有的牵挂
    若有天我不复勇往 能否坚持走完这一场
    踏遍万水千山总有一地故乡

    她走在马蹄的余声中
    夕阳燃烧离别多少场
    她向陌生人们解说陌生人的风光
    等她归来坐下对我讲
    故人旧时容颜未沧桑
    我们仍旧想要当初想要的不一样

## 进入正题

网易云音乐有两种外链播放器插件，一种是iframe：

    <iframe frameborder="no" border="0" marginwidth="0" marginheight="0" width=330 height=86 src="http://music.163.com/outchain/player?type=2&id=29734857&auto=1&height=66"></iframe>

另一种是flash插件：

    <embed src="http://music.163.com/style/swf/widget.swf?sid=29734857&type=2&auto=1&width=320&height=66" width="340" height="86"  allowNetworking="all"></embed>

经过测试flash是可以在我的surface+windows+chrome上使用的，但是很多平台都不支持flash了，所以经过各种考虑【为了逼格】，决定还是试一下iframe。

直接使用iframe是会直接显示出代码，而不会显示播放器的，下面写出修改的地方：

把iframe的width和height标签的值加上双引号就可以了，顺便把自动播放给关掉，就像这样：

    <iframe frameborder="no" border="0" marginwidth="0" marginheight="0" width="330" height="86" src="http://music.163.com/outchain/player?type=2&id=29734857&auto=0&height=66"></iframe>

效果就是下面这样的。

<iframe frameborder="no" border="0" marginwidth="0" marginheight="0" width="330" height="86" src="http://music.163.com/outchain/player?type=2&id=29734857&auto=0&height=66"></iframe>

同样的也可以应用播放列表：

<iframe frameborder="no" border="0" marginwidth="0" marginheight="0" width="330" height="450" src="http://music.163.com/outchain/player?type=0&id=48865558&auto=0&height=430"></iframe>


## 扯淡：

这周碰到两个渠道的SDK，写的太烂了，还得接，真是悲伤。github一点没更新，买了epiphone les paul穷的跟个狗一样。顺便向网易云音乐提交了两个歌词错误。