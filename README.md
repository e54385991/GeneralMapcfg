

这是其他服务器地图参数 或者翻译 
ZE服务器请点这里 https://github.com/MapTextLang/MapTextLang


### 文件验证同步是否成功判断
1. sm_gitsync_check_cureentmap_user 指令可以检查同步情况含文件MD5/CRC 修改时间等 [权限等级:任何玩家 间隔限制 300秒]
2. sm_gitsync_check_cureentmap 指令可以检查同步情况含文件MD5/CRC 修改时间等 [权限等级:OP 或 已认证Mapper用户]


# X社区 地图翻译 / stripper /
---
这是X社区 地图翻译 / Entwatch / stripper mapcfg(地图参数) 或者其他翻译 GIT仓库。

地图翻译/stripper/mapcfg 支持所有类型服务器。

只要对应服务器具备相应地图就会同步本仓库数据，其他服务器不会产生影响。

## 目录说明
---
+ mapcfg      ->地图参数         【已支持自动同步】
+ mappool     ->地图池控制系统   【已支持自动同步】
+ maptext     ->地图翻译         【已支持自动同步】
+ prophurt    ->躲猫猫地图道具   【已支持自动同步】

## 游戏中自动同步方法
---
1. 更新/添加修改/你想要的 通过创建 [Pull requests](https://github.com/MapTextLang/MapTextLang/pull/new/master).

2. 当您提交Pull Request后 在管理通过后 在论坛会 [显示事件](https://bbs.93x.net/plugin.php?id=xnet_events:xnet_events). 应该会显示事件 如果没有显示 可能没有成功 请加上一些无用注释 如//再提交一次 和原不同即可)

3. 游戏服务器会每隔地图更换 自动检测修改并同步 op / mapper可以输入 !git_update 强行同步 【请不要在 修改后的 10分钟内输入 否则无法拉到新数据 因为缓存】

版本会自动变化以让游戏服务器检测 [GIT版本查看地址](http://bd.93x.net/maptexthook/git_version.txt) （触发 合并审核 / 修改 / 添加 事件后会自动修改 +1 换图后 如果服务器检测到版本不同那么会拉取需要更新的数据）

## 地图修改服务器参数/或指令拦截
---

### 地图参数拦截功能

`sm_block_command` 想要拦截参数关键词
`sm_block_command zr_infect_spawntime` 就可以禁止掉地图修改尸变时间

### [用法演示](https://github.com/MapTextLang/MapTextLang/blob/master/mapcfg/ze_grau_a03_4f.cfg#L15-L17)
---

默认拦截有关 "STEAM_" 所有关键词
在mapcfg中添加 `mapcommandblock_enable 0` 则不会阻挡地图操作命令（默认 1） 此CVAR安全锁定 只能由配置文件修改

但即使地图有白名单参数 也拒绝 kick ban操作 此屏蔽强制执行

通过 sm_block_command "增加想要的参数命令关键词"

捕捉地图在做什么命令？
使用 `sm_showmapcmd` 开关捕捉 信息输出到控制台

## 翻译文件禁止事项
---
1. 禁止使用特殊字符 如`/` `\` `＂` `“`　等符号
2. 禁止删除引号 `"` 删除括号如`{` `}`．
3. 禁止修改地图主语句, 如: `*** The Train Will Leave in 5 seconds ***`
4. 禁止换行


### 仓库维护 一般每月一次

编辑 README.md 在尾部 添加任何无用注释内容
编辑原因填写为 "triggercleanup" 即可清理同步缓存
如果因为文件名错误  或者 小大写错误 则必须执行清理同步缓存

#trigger update13
test for web hook
#push trigger update p5
triggercleanup 最后维护
2021年6月8日10:00:0
#########5triggercleanup
#1Trigger P
