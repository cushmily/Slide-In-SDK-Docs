# 快速开始

> 这篇文章将从安装开始，一步一步指引开发者如何使用Slide-In SDK。



## 前置需求

在开始之前，请先确保生产环境满足以下条件。

### 硬件需求

- 三星Galaxy S8 / 三星Galaxy S9
- 至少一个Marker或者Marker组合

### 软件需求

- Android SDK
- Unity 2017.4.17 f1 / Unity 2018.3.x （其他版本可能会遇到头部旋转不正确的情况，请自己测试）
- [Vysor](https://www.vysor.io) (**可选项**， 用于远程操作Android设备，提升开发效率)



## 安装步骤

### 获取SDK

你可以选择将Slide-In SDK 仓库整个Clone 下来至本地：

```bash
$ git clone git@github.com:Ximmerse/SlideInSDK.git
```



### 安装SDK

将项目仓库中的[`./UnitySDK/Assets/`](https://github.com/Ximmerse/SlideInSDK/tree/master/UnitySDK/Assets/) 内所有文件复制至一个空白项目中的`Assets/Plugins/`文件夹中即可。



### 目录说明

- _DemoAssets

  SDK的示例代码以及实例资源。

- Controller Management

  蓝牙控制器管理工具的源码。

- [LunarConsole](https://assetstore.unity.com/packages/tools/gui/lunar-mobile-console-free-82881)

  一个用于在手机上显示控制调试信息的免费插件，用于提高开发效率。

- **Android/x86_64**

  在Android/Windowsx86的终端上的Slide-In 硬件使用库。（OSX暂时不支持）

- **SlideInSDK**

  Slide-In SDK 上层开发接口部分源码。

- **PEPlugins**

  为Slide-In SDK HLAPI提供基础建设，同时提供了很多辅助开发的工具。



### 项目设置

安装完SDK后，我们需要对进行一些设置以确保SDK正常运行。

首先在`PlayerSettings`中的`Resolution and Presentation`我们需要将手机的默认旋转方向设置成为横向右向。

![](https://ximmerse-1253940012.cos.ap-guangzhou.myqcloud.com/slide-in-sdk/device-orientation.png)

然后在`XR Settings`中按照下图中的设置，一次增加`None`和`Cardboard`选项。

!> **None**选项不能省略

![](https://ximmerse-1253940012.cos.ap-guangzhou.myqcloud.com/slide-in-sdk/xr-settings.png)

最后我们通过窗口菜单`Tools/Slide in/Initialize SDK`初始化一下Slide-In SDK，就完成了整个项目的设置。

![](https://ximmerse-1253940012.cos.ap-guangzhou.myqcloud.com/slide-in-sdk/init-sdk.png)

## 实例说明

**Bench Marker**

Bench Marker的使用示例说明场景。

**Bench Marker Match Scale Content**

·Bench Marker的使用示例说明场景，包含对`Bench Marker` 建立的原点坐标系缩放的示例。





## 使用实例

> `PEPlugins`中拥有了BuildManager工具辅助快速打包，在快速开始的示例中，我们将会使用预设的`BuildPreset`。

首先进入`Tools/PolyEngine/Build Manager`

![](https://ximmerse-1253940012.cos.ap-guangzhou.myqcloud.com/slide-in-sdk/buildmanager.png)

选择`Tag Tracking`这个Preset，并且点击Load Preset

![](https://ximmerse-1253940012.cos.ap-guangzhou.myqcloud.com/slide-in-sdk/build-manager-settings.png)

加载完Preset后，工具会帮我们设置好所有的配置。

这时候我们可以进入`Player Settings`进行打包。

![](https://ximmerse-1253940012.cos.ap-guangzhou.myqcloud.com/slide-in-sdk/build-project.png)

安装apk到手机上，将手机插入头显并且连接，即可开始完整的测试Marker的追踪功能了。

