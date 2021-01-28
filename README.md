# proj67-linux-randconfig-test-on-RespberryPi-or-RV

### 项目名称

Linux内核randconfig启动测试 @ 树莓派/RISC-V

### 项目描述

Linux 内核有超过9000个编译选项，它们的随机组合是一个天文数字。
本项目的目标：有效组织测试，充分暴露、定位、报告在不同组合下的内核启动问题。

Compass-CI 是一个系统级测试平台。为包括内核在内的各类开源软件（来自 Github, Gitee, Gitlab 等托管平台）提供测试、故障辅助定界服务和基于历史数据的分析服务。(https://compass-ci.openeuler.org/)

Compass-CI平台目前支持的测试机主要是服务器和虚拟机。还需要引入树莓派/RISC-V等硬件作为测试机，以实现多样化的测试覆盖。
Compass-CI平台目前支持linux kernel的randconfig build test。还需要进一步引入randconfig boot test，以捕捉各类硬件上的启动问题。
在发现启动问题后，还需要实现bisect来自动定位引入问题的first bad commit.

本项目的目标是在树莓派或者RISC-V硬件上实现全流程Linux内核randconfig启动测试。

### 所属赛道

2021全国大学生操作系统比赛的“OS功能设计”赛道

### 参赛要求

- 以小组为单位参赛，最多三人一个小组，且小组成员是来自同一所高校的本科生（2021年春季学期或之后本科毕业的大一~大四的学生）
- 如学生参加了多个项目，参赛学生选择一个自己参加的项目参与评奖
- 请遵循“2021全国大学生操作系统比赛”的章程和技术方案要求

### 项目导师

刘隐四 曹学亮

* email liuyinsi@163.com
* email caoxl78320@163.com


### 难度

中等


### 特征

- 在树莓派或RISC-V硬件上完成全流程内核randconfig启动测试

### 文档

### License

MulanPSL-2.0 (https://opensource.org/licenses/MulanPSL-2.0)

## 预期目标

### 注意：下面的内容是建议内容，不要求必须全部完成。选择本项目的同学也可与导师联系，提出自己的新想法，如导师认可，可加入预期目标


### 在raspberry/riscv硬件上完成全流程内核randconfig启动测试

在Compass CI现有功能基础上，实现
* 树莓派/RISC-V上可启动randconfig内核的构建
* 树莓派/RISC-V的openEuler rootfs制作
* 树莓派/RISC-V上启动内核+rootfs
* 树莓派/RISC-V的crash自动重启
* 树莓派/RISC-V的串口dmesg收集
* dmesg错误的自动bisect定位
* 自动向内核社区发送email报告

功能设计应当通用化和实用化。
功能上线后，希望每周对内核社区报告1个以上kernel boot bugs.
