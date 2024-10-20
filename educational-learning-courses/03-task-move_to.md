# 分析 move_to 系统调用错误的修复

## 信息

- 任务ID：#5
- 导师：[Samuka007](https://github.com/Samuka007), Sig-Network, samuka007@qq.com
- bbs链接：https://bbs.dragonos.org.cn/t/topic/369

## 任务说明

查看bug修复的commit，知道为什么修改后行为正常了，[相关PR](https://github.com/DragonOS-Community/DragonOS/pull/673)

## 初始化环境配置

> 这里是其中一种基于worktree的分离做法，你也可以直接clone两次然后分别checkout到不同的commit

首先 clone repo，但先不要像教程里那样跑bootstrap.sh部署环境，因为这个pr所属的开发环境比较旧，新旧工具链不兼容。进入repo文件夹根目录后，创建以下两个commit的worktree

- 39203abc4c0c31f8f86586db75bd73ebc6194bf1
- 9d9a09841ce2d650a41fed776916c0a11d52f92e

然后像[部署文档](https://docs.dragonos.org.cn/introduction/build_system.html)那样，进入 new/old 的 worktree 文件夹，然后执行命令

```bash
cd tools && bash bootstrap.sh
```

这样就部署好了你的工作环境，并且可以同时在old/new分支之间进行比较/开发

## 任务要求

- 理解 move_to 在index node中的实现，比较新旧commit的区别
- 有能力的可以再对文件系统相关的部分进行理解、解构乃至完善。