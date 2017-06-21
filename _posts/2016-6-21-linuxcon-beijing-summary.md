---
layout: post
title: LC3会议-NEAOSS大师训练营记录
comments: true
---

原来没有计划参加这次的LinuxCon, 感觉涉及的面比较大，有不少是和容器及虚拟化相关的，和我嵌入式以及内核开发方面的交集不大。不过也许是缘分吧，得知这次有机会参加NEAOSS训练营的活动，并和Greg以及Ted面对面交流，还是决定参加。

参加前在shed上定了个日程:
https://lc3china2017.sched.com/yangwenbo

有心人会发现除了Linus等核心maintainer, 一些重量级的人物也会以听众身份低调参加。比如这位Allen，现场穿了一件GCC文化衫，安静地坐在那里聆听思考记录。
https://lc3china2017.sched.com/allensamuels

这是之前他在LinuxCon做的Ceph和Flash方面的分享：
https://www.linux.com/videos/ceph-and-flash-allen-samuels-western-digital


### Linux foundation中国分部
参加培训不要熬夜了。

### Ted关于Ext4的分享
lazy ext4 first principle , dirty hands to avoid dirty hands, read the paper

### Reproducible Build
Reproducible build, diffscope

### Enhancing Linux Security with the TPM
这个分享整体效果很好，可惜时间短些。
利用每个主板都有的TPM芯片，代替UbiKey等实体密钥。
还听了Matthew Treisnish的一个分享，改造老旧公寓里的温度控制器。/* 生活中遇到的不舒服的地方尝试用代码去改变，开源出来，无心插柳，linux kernel, latex */

### NEAOSS 训练营
重头，是和Ted以及Greg的互动, 直接感受到两位人物精力的旺盛，开放的心态，认真回答每一个问题。问答环节：
* horse for course, 技术的使用场景。 /* 思考domain specific language/hard ware/file system, app平台化，平台app 化，抽象层的增减。*/
* Linux文件系统的test suite, 是源于神奇公司SGI的xfstests suite，测过再提交，maintainer的精力有限;
* 提要求不如提patch;

在回答一个同学关于阅读内核原代码的建议时，Ted讲了几点入门的要诀：
* 全部通读在目前很难。建议找到感兴趣的子系统，读这个特定部分的代码，自然延伸到和它邻接和互动的模块；
* 尝试做一些简单的patch;
* 比如一些历史遗留的文件系统；
* 可以尝试解决test failure，比如XFS tes和LTP test;
* 不要只是读，要动手参与贡献！

之后和组织者互动，峰光，陈教授的总结。

## 给大会组织者的小建议
即使小会场也能录音录像，作为资料。另外代码之外交流的细节体现功力积累和做事的方法风格，这些都是很好的养料。

