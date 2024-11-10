
# DragonOS的内核初始化(x86_64架构)

## 信息

- 任务ID: #4
- 导师名单
  - [黄铭涛](https://github.com/1037827920): Sig-Cloud-Provider, 1037827920@qq.com
- 难度：2颗星
- 辅导时间：7天
- 涉及的代码仓库: [DragonOS](https://github.com/DragonOS-Community/DragonOS)
- 主要涉及的文件:
  - kernel/src/arch/x86_64/init/mod.rs
  - kernel/src/init/init.rs
  - kernel/src/mm/init.rs
  - kernel/src/filesystem/vfs/core.rs
  - kernel/src/driver/base/init.rs
  - kernel/src/sched/mod.rs
  - kernel/src/time/timekeeping.rs
  - kernel/src/process/kthread.rs
- bbs链接: https://bbs.dragonos.org.cn/t/topic/372

## 任务的简介

本任务旨在引导新加入的社区成员通过阅读DragonOS的内核初始化代码，理解其启动过程。从kernel/src/arch/x86_64/init/mod.rs的kernel_main开始阅读，重点分析kernel/src/init/init.rs文件中的关键函数**do_start_kernel**，学员将学习内核初始化涉及的各个步骤和组件，为云移植工作打下基础。


## 任务目标

学习目标: 
- 涉及源码的哪些方面
  - 分析do_start_kernel函数的实现，理解各个初始化步骤的作用和顺序
  - 探索DragonOS在x86_64架构下的特殊初始化步骤和条件编译相关内容
- 学员能够从中学到什么
  - 掌握DragonOS内核初始化的基本流程
  - 理解各个初始化函数的功能和调用顺序
  - 学习如何通过阅读和分析源码来理解复杂系统的工作原理
- 学员应当完成哪些思考任务 
  - 分析每个初始化函数的作用及其对整个系统启动的影响
  - 各个部分的初始化顺序重要吗？为什么？
  - 思考在云环境下，哪些初始化步骤可能需要进行调整或兼容性处理
- 学员需要提交哪些材料
  - 源码阅读报告，详细描述do_start_kernel函数的各个步骤的初始化及其作用，对于不是do_start_kernel函数中的代码，只需要理解代码的作用即可
  - 思考任务