小开特供版Alas：

特性：

重启时，解决GG弹窗。

可在Alas内配置的倍率小开。

一个简单的仪表盘

出现未知界面，直接重启。 

敏感项目自动重启并以正常数据攻打。

敏感项目，前排战力大于16500（可配置）强制重启。

紧急委托前排可以选择更换为10级以上的驱逐舰。

可以选择在一键退役时尝试不保留没满星的舰船（危险选项！操作前阅读说明）

使用方法：

1，将alas库地址修改为本地址

2，修改小开配置文件，建议“每次重启Alas时重启”一项打开，否则可能会出现记录的状态与实际不同。虽然还有最后的验证防止打信标和演习暴毙，但不保证一定安全。

![image](https://user-images.githubusercontent.com/60862861/215345815-4eac0490-cda6-4b01-be2a-31f85da366f5.png)

3，将悬浮窗放在石油上，保证遮盖，不要隐藏以免出现后宅心情幸运币导致的误触（使用截图策略时）

![image](https://user-images.githubusercontent.com/60862861/213346533-a2fd836a-a603-4ce0-b75f-8169d90e1884.png)

4，执行一次lua，保证点执行脚本时如下图（使用截图策略时）

![image](https://user-images.githubusercontent.com/60862861/215345768-1c1c3342-44be-4ab0-bcc5-a5360a4e6451.png)

5，调整你的模拟器，开发者设置中，最小宽度为480（使用截图策略时）

6，GG明确表明蓝叠模拟器很慢。加上目前水平太菜无法解决蓝叠时常出现的UI Automator2无法使用的问题。加上蓝叠不能导入文件夹+本人网速极慢。因此若出现问题，不作任何支持。你可以使用截图策略进行最后的挣扎。

7，祝您使用AlasGG小开愉快。

## 安装 Installation [![](https://img.shields.io/github/downloads/LmeSzinc/AzurLaneAutoScript/total?color=4e4c97)](https://github.com/LmeSzinc/AzurLaneAutoScript/releases)

详见 [中文安装教程](https://github.com/LmeSzinc/AzurLaneAutoScript/wiki/Installation_cn)，包含自动安装教程，使用教程，手动安装教程，远程控制教程。



## 正确地使用调度器

- **理解 *任务* 和 *调度器* 的概念**

  在 Alas 中每个任务都是独立运行的，被一个统一的调度器调度，任务执行完成后会自动设置这个任务的下一次运行时间。例如，*科研* 任务执行了一个 4 小时的科研，调度器就会把 *科研* 任务推迟 4 小时，以达到无缝收菜的目的。

- **理解 *自动心情控制* 机制**

  Alas 的心情控制以预防为主，不会等到出现红脸弹窗才去解决，这样可以保持心情值在 120 以上，贪到 20% 的经验。例如，当前心情值是 113，放置于后宅二楼（+50/h），未婚（+0/h），Alas 会等到 12 分钟之后，心情值回复到 120 以上再继续出击。而在这个等待的期间，Alas 也会穿插执行其他任务。

- **正确地使用调度器**

  调度器的 **错误使用方法是只开一两个** 任务，手动管理任务或开关 Alas，调度器的 **正确使用方法是启用全部** 你觉得可能有用的任务，让调度器自动调度，把模拟器和 Alas 都最小化到托盘，忘记碧蓝航线这个游戏。



## 修改游戏设置

对照这个表格修改游戏内的设置，~~正常玩过游戏的都这么设置~~。

> 对着改的意思是，这是统一的标准，照着给定的内容执行，不要问为什么，不允许有不一样的。

主界面 => 右下角：设置 => 左侧边栏：选项

| 设置名称                            | 值   |
| ----------------------------------- | ---- |
| 帧数设置                            | 60帧 |
| 大型作战设置 - 减少TB引导           | 开   |
| 大型作战设置 - 自律时自动提交道具   | 开   |
| 大型作战设置 - 安全海域默认开启自律 | 关   |
| 剧情自动播放                        | 开启 |
| 剧情自动播放速度调整                | 特快 |

主界面 => 右下角：建造 => 左侧边栏： 退役 => 左侧齿轮图标：一键退役设置：

| 设置名称                                                 | 值               |
| -------------------------------------------------------- | ---------------- |
| 选择优先级1                                              | R                |
| 选择优先级2                                              | SR               |
| 选择优先级3                                              | N                |
| 「拥有」满星的同名舰船时，保留几艘符合退役条件的同名舰船 | 不保留           |
| 「没有」满星的同名舰船时，保留几艘符合退役条件的同名舰船 | 满星所需或不保留 |



## 如何上报bug How to Report Bugs

在提问题之前至少花费 5 分钟来思考和准备，才会有人花费他的 5 分钟来帮助你。"XX怎么运行不了"，"XX卡住了"，这样的描述将不会得到回复。

- 在提问题前，请先阅读 [常见问题(FAQ)](https://github.com/LmeSzinc/AzurLaneAutoScript/wiki/FAQ_en_cn)。
- 检查 Alas 的更新和最近的 commit，确认使用的是最新版。
- 上传出错 log，在 `log/error` 目录下，以毫秒时间戳为文件夹名，包含 log.txt 和最近的截图。若不是错误而是非预期的行为，提供在 `log` 目录下当天的 log和至少一张游戏截图。



## 已知问题 Known Issues

- **无法处理网络波动**，重连弹窗，跳小黄鸡。
- **在极低配电脑上运行可能会出现各种问题**，极低配指截图耗时大于1s，一般电脑耗时约0.5s，高配耗时约0.3s。
- **演习可能SL失败**，演习看的是屏幕上方的血槽，血槽可能被立绘遮挡，因此需要一定时间（默认1s）血量低于一定值（默认40%）才会触发SL。一个血皮后排就有30%左右的血槽，所以有可能在 1s 内被打死。
- **极少数情况下 ADB 和 uiautomator2 会抽风**，是模拟器的问题，重启模拟器即可。
- **拖动操作在模拟器卡顿时，会被视为点击**



## 模拟器问题 Emulator Issues

见 [设备支持文档](https://github.com/LmeSzinc/AzurLaneAutoScript/wiki/Emulator_cn)，包含模拟器运行、云手机运行以及解锁各种骚方式运行。



## Alas 社区准则 Alas Community Guidelines

见 [#1416](https://github.com/LmeSzinc/AzurLaneAutoScript/issues/1416)。



## 文档 Documents

[海图识别 perspective](https://github.com/LmeSzinc/AzurLaneAutoScript/wiki/perspective)

`海图识别` 是一个碧蓝航线脚本的核心，如果只是单纯地使用 `模板匹配 (Template matching)` 来进行索敌，就不可避免地会出现 BOSS被小怪堵住 的情况。 Alas 提供了一个更好的海图识别方法，在 `module.map_detection` 中，你将可以得到完整的海域信息，比如：

```
2020-03-10 22:09:03.830 | INFO |    A  B  C  D  E  F  G  H
2020-03-10 22:09:03.830 | INFO | 1 -- ++ 2E -- -- -- -- --
2020-03-10 22:09:03.830 | INFO | 2 -- ++ ++ MY -- -- 2E --
2020-03-10 22:09:03.830 | INFO | 3 == -- FL -- -- -- 2E MY
2020-03-10 22:09:03.830 | INFO | 4 -- == -- -- -- -- ++ ++
2020-03-10 22:09:03.830 | INFO | 5 -- -- -- 2E -- 2E ++ ++
```

更多文档，请前往 [WIKI](https://github.com/LmeSzinc/AzurLaneAutoScript/wiki)。



## 参与开发 Join Development

Alas 仍在活跃开发中，我们会不定期发布未来的工作在 [Issues](https://github.com/LmeSzinc/AzurLaneAutoScript/issues?q=is%3Aopen+is%3Aissue+label%3A%22help+wanted%22) 上并标记为 `help wanted`，欢迎向 Alas 提交 [Pull Requests](https://github.com/LmeSzinc/AzurLaneAutoScript/pulls)，我们会认真阅读你的每一行代码的。

哦对，别忘了阅读 [开发文档](https://github.com/LmeSzinc/AzurLaneAutoScript/wiki/1.-Start)。



## 相关项目 Relative Repositories

- [AzurStats](https://azur-stats.lyoko.io/)，基于 Alas 实现的碧蓝航线掉落统计平台。
- [AzurLaneUncensored](https://github.com/LmeSzinc/AzurLaneUncensored)，与 Alas 对接的碧蓝航线反和谐。
- [ALAuto](https://github.com/Egoistically/ALAuto)，EN服的碧蓝航线脚本，已不再维护，Alas 模仿了其架构。
- [ALAuto homg_trans_beta](https://github.com/asd111333/ALAuto/tree/homg_trans_beta)，Alas 引入了其中的单应性变换至海图识别模块中。
- [PyWebIO](https://github.com/pywebio/PyWebIO)，Alas 使用的 GUI 库。
- [MaaAssistantArknights](https://github.com/MaaAssistantArknights/MaaAssistantArknights)，明日方舟小助手，全日常一键长草，现已加入Alas豪华午餐 -> [MAA 插件使用教程](https://github.com/LmeSzinc/AzurLaneAutoScript/wiki/submodule_maa_cn)

