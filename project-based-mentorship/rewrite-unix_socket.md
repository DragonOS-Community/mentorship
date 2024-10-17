# 重写部分UNIX socket

## 信息

- 任务ID: #7
- 导师: [smallcjy](https://github.com/smallcjy), Sig-Network, 2628035541@qq.com
- bbs链接: https://bbs.dragonos.org.cn/t/topic/373
- 难度: 中等

**前置学习目标：**

rust基本语法、智能指针以及常见锁的使用、tcp握手流程及其状态机

**重写内容：**

重写unix stream socket 握手过程。代码位于net/socket/unix下，需要尝试重写Inner内的Init、Listener、Connected状态结构体及其涉及建立握手的方法，重写Socket接口中的bind接口、connect接口、listen接口、accept接口。