---
layout: post
title: LC3会议-NEAOSS大师训练营记录
comments: true
---

原来没有计划参加这次的LinuxCon, 感觉涉及的面比较大，有不少是和容器及虚拟化相关的，和我嵌入式以及内核开发方面的交集不大。不过也许是缘分吧，得知这次有机会参加NEAOSS训练营的活动，并和Greg以及Ted面对面交流，还是决定参加。

参加前在shed上定了个[日程](https://lc3china2017.sched.com/yangwenbo)

有心人会发现除了Linus等核心maintainer, 一些重量级的人物也会以听众身份低调参加。比如这位[Allen](https://lc3china2017.sched.com/allensamuels)，现场穿了一件GCC文化衫，安静地坐在那里聆听思考记录。

之前他在LinuxCon做的[Ceph和Flash方面的分享](https://www.linux.com/videos/ceph-and-flash-allen-samuels-western-digital)


### NEAOSS 训练营
是我这次活动的重头。和Ted以及Greg的互动, 直接感受到两位人物精力的旺盛，开放的心态，认真回答每一个问题。

问答环节：
* horses for courses, 技术的使用场景。 /* 思考: domain specific language/hard ware/file system, app平台化，平台app化，抽象层的增减。*/
* Linux文件系统的测试集, 是源于神奇公司SGI的[xfstests suite](https://github.com/tytso/xfstests-bld/blob/master/Documentation/what-is-xfstests.md)，Ted要求社区的贡献者在测试集测过再提交，maintainer的精力有限;
* 提要求不如提patch;

在回答一个同学关于阅读内核原代码的建议时，Ted讲了几点入门的要诀：
* 全部通读在目前很难。建议找到感兴趣的子系统，读这个特定部分的代码，自然延伸到和它邻接和互动的模块；
* 尝试做一些简单的patch;
* 比如一些历史遗留的文件系统；
* 可以尝试解决test failure，比如XFS tes和LTP test;
* 不要只是读，要动手参与贡献！

之后和峰光，陈钟教授的互动。

其它几个比较感兴趣的分享：
### Linux foundation中国分部
参加基金会的培训再也不用熬夜了。

### Ted关于Ext4的分享
lazy-ext4, 通过对底层硬件特性的把握，找到历史实现中不再合适的地方，get hands dirty 从而实现avoid “dirty hands”。相关[论文](https://www.usenix.org/system/files/conference/fast17/fast17-aghayev.pdf)发在了usenix的会上。

### Reproducible Build
来自Debian的Chris Lamb。无论何时何地编译，同样的代码产生同样的二进制包，这对嵌入式应用和安全有用。相关[网站](https://reproducible-builds.org/)，还开发了一个包diff工具甚至有在线版，[diffscope](https://diffoscope.org/)

### Enhancing Linux Security with the TPM
来自IBM的James Bottomley, 这个分享整体效果很好，可惜时间短些。

利用每个主板都有的TPM芯片，代替YUBIKEY等实体密钥。

[手机录音](https://soundcloud.com/user-796021324/james_bottomley_tpm_linux_security_lc3_beijing_2017)
作者用impress.js作的[slides](http://www.hansenpartnership.com/Impress-Slides/LinuxCon-China-2017/#/begin)

还听了也是IBM来的Matthew Treisnish的一个分享，改造老旧公寓里的温度控制器。/* 思考： 这些项目也许份量难度不同，但相同的是生活工作中遇到的不舒服的地方尝试用代码去改变，开源出来，无心插柳，例如linux kernel, latex */

### 64-bit ARM Unikernels on uKVM
黄宇强同学的在线[笔记](https://hackmd.io/s/BkoYAUrQb)

## 给大会组织者的小建议
即使小会场也希望能够录音录像，作为资料。代码之外交流的细节，体现功力积累和做事的方法风格，对我们都是养料。

