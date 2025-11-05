# 运动XX校园Xposed辅助模块

## 项目背景

为了让Dgut的轮滑仔们大晚上可以的一起去刷跑，于是这个项目就诞生了。主要的目的是将现在xx的*有序点位*换回原来的*无序点位*，目前只是将点位模式更换了，所以有一定的检测风险。在未来，希望有精力去添加修改点位顺序的功能，这样可以降低一定风险。

## 功能
- 修改跑步模式
  
  > 有序点位和无序点位
  
- 取消夜间跑步限制

  > 该功能会自动切换到无序模式，可以使用**修改跑步模式**修改成有序点位

- 关闭定位信息检测

  > 该功能在定位信息弱的时候可以减少一定的GPS信号弱的警告

- 关闭点位信息检测

  > 完全跳过点位信息检测，甚至在GPS信号没有的时候都能保持跑步模式，但是这样并不能完成跑步任务，所以这个功能不建议启动，反而会因为无法了解自身的GPS状态而导致白跑

- 去广告

  > 本项目是直接停止广告的相关活动、弹窗来去掉广告，所以理论上说，并不容易被后台运控开启广告。
  
- 强制返回取消弹窗

  > 这个目前作用不大，主要是去弹窗广告的备选方案
  
## 编译

项目已配置GitHub Actions自动编译工作流，每次推送代码到main/master分支或提交Pull Request时会自动编译。

### 自动编译
1. 推送代码到main或master分支
2. 在GitHub仓库的Actions标签页查看编译进度
3. 编译完成后，在Actions运行记录中下载生成的APK文件（app-release artifact）

### 手动编译
你也可以手动触发编译：
1. 进入GitHub仓库的Actions标签页
2. 选择"Android CI"工作流
3. 点击"Run workflow"按钮

### 本地编译
如需本地编译，请确保已安装JDK 17和Android SDK：

```bash
git clone git@github.com:LiuYiGL/RunWorldSchoolMod.git
cd RunWorldSchoolMod
./gradlew assembleRelease
```

编译完成后，APK文件位于 `app/build/outputs/apk/release/app-release-unsigned.apk`

## 安装

本项目仅进行开源处理，并不对使用者负责。且成果仅在内部使用，如需使用也可以自行`git clone`本仓库进行编译apk使用，切勿进行广泛流传。

## 使用

该辅助为Xposed模块，使用前需对Xposed框架有一定了解。
具体使用教程参照其他Xposed插件，本项目推荐用Lsposed框架进行安装，或者使用Lspactch对宿主App进行修补

> 详情 [Lsposed](https://github.com/LSPosed/LSPosed)、[Lspatch](https://github.com/LSPosed/LSPatch)

## 感谢

- 首先肯定是[Lsposed](https://github.com/LSPosed/LSPosed)框架，免重启应用模块真的帮了我的大忙

- 其次就是KyuubiRan的[EzXHelper](https://github.com/KyuubiRan/EzXHelper)提供了很多的工具类可以让我专注于逻辑的编写

------
> 作者算是小白一个，第一次在GitHub上有自己的开源项目，如果有很多不太规范的地方欢迎积极不吝赐教，感谢支持！
