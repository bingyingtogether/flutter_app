### 为什么我们需要跨平台开发？
> 本质上，跨平台开发是为了增加代码复用，减少开发者对多个平台差异适配的工作量，降低开发成本，提高业务专注的同时，提供更好的体验。通俗了说就是：省钱、偷懒。

就目前来说，跨平台的开发主要有三个：
1. react native、weex均使用JavaScript作为编程语言，目前JavaScript在跨平台开发中，可谓占据半壁江山，大有“一统天下”的趋势；

2. flutter是使用的Dart作为编程语。

##### 1.react native
Facebook推出的，JSCore引擎，React设计模式
> “Learn once, write anywhere” ，代表着 Facebook对 react native 的定义:学习 react ，同时掌握 web 与 app 两种开发技能。

RN 构建的应用使用的实际控件是原生控件，用户拥有与原生应用相近的使用体验。 对于 React Native 抽象层无法满足的应用程序，仍然需要原生开发定制。

如果需要与大量定制的原生代码相结合，那么在 React Native 的抽象层中工作的好处就会减少，这种情况下，原生开发会更有优势。而且RN的性能这块比原生也是差蛮多的。

##### 2.Weex:
阿里推出来的，JS V8引擎，Vue设计模式
> “Write once, run everywhere”：
>
> Weex 的结构是解耦的，渲染引擎与语法层是分开的，目前主要支持 Vue.js 和 Rax 这两个前端框架。Weex 在 iOS 和 Android 上都实现了一个渲染引擎，并提供了一套基础的内置组件。基于这些组件，你可以用JS封装更多的上层组件。 （当然，现实有时很骨感）因为就性能和兼容性上实际上是没有想象那么美好的

##### 3.Flutter：
谷歌推出来的，Engine引擎，响应式设计模式
> 真正做到了写一次，处处运行，跨平台兼容性非常好，而且性能也是这三个中最好的

Flutter 主要分为 Framework 和 Engine，我们基于Framework 开发App，运行在 Engine 上。Engine 是 Flutter 的独立虚拟机，由它适配和提供跨平台支持。

得益于 Engine 层，Flutter 甚至不使用移动平台的原生控件， 而是使用自己 Engine 来绘制 Widget，而 Dart 代码都是通过 AOT 编译为平台的原生代码，所以 Flutter 可以直接与平台通信，不需要JS引擎的桥接。

#### 未来趋势展望
##### RN
社区：已有各类丰富的第三方库

“Airbnb（爱彼迎） 宣布放弃使用 React Native，回归使用原生技术” : Airbnb 作为 react native 平台上最大的支持者之一，其开源的lottie 同样是支持原生和 react native。

Airbnb 在宣布放弃的文中，也对 react native 的表示了很大量的肯定，而使得他们放弃的理由，其实主要还是集中于项目庞大之后的维护困难，第三方库的良莠不齐，兼容上需要耗费更多的精力导致放弃。

##### weex
2016年开源至今，社区和各类文档都显得有点疲弱，作为跨平台开发人员，大多时候肯定不会希望，需要频繁的自己增加原生功能支持，因为这样的工作一多，反而会与跨平台开发的理念背道而驰，带来开发成本被维护难度增加。

##### Flutter
Flutter现在还没出正式版，但是以谷歌的号召力，flutter现在就已经很火了，开发人员已经有了大量可以使用的包和插件。并且谷歌的新系统**Fuchsia** 使用了该公司自有的“Escher”渲染器和“Flutter”SDK 。前者主要负责在屏幕上绘制 Material Design 元素，后者则用于跨平台代码的实现，以方便 iOS 和 Android 的开发者们。这些集合到一起难免让你怀疑 Android 是否要被谷歌抛弃的想法。

或者如今先在 Android 等平台上推广 Flutter 与 Dart，就是为了以后更好的过渡到新系统上，毕竟开发者是操作系统的生命源泉之一。而 Java 与 JVM 或许会被谷歌完全抛开。
**(Little Kernel 微内核)**



dart从11年出现，刚开始他的目的就是要干掉JS，但是一直没成功，用的人也少，但是谷歌一直坚持在用，Google对外宣布数据：

2016年谷歌的AdWords、AdSense和Fiber项目团队开始把Dart融入他们的前端应用开发。一项内部报告表明，Dart可以帮助他们提升25%到100%的前端开发效率。谷歌内部的Dart代码量比去年增长了3.5倍

Google从前端，到新开发的系统，到我们现在接触到的flutter都是使用dart，足以见得，google对dart的重视。

但换句话来说，只要有一环能够成功，那么整个环路都能活起来。

而flutter可以说是谷歌的出口，因为跨平台肯定是未来的趋势，而现在flutter可以说是当前市面上出来的最好的跨平台语言了，当然咯，能不能成功还是要看谷歌的推广了，毕竟语言这东西不是好就一定有人用。

## Flutter发展史

- 2015 年 4 月，Flutter（最初代号 Sky）在 Dart Developer Summit 上展示
- 2015 年 11 月，Sky 重命名为 Flutter
- 2018 年 2 月，在 2018 年移动世界大会上 Flutter beta 1 官宣
- 2018 年 4 月，Flutter beta 2 官宣
- 2018 年 5 月，在 Google I / O 上 Flutter beta 3 官宣。
- 2018 年 6 月，Flutter 预览版发布

## Flutter的一些特性

首先我们来说说为什么flutter会选择Dart语言

1. Dart运行时和编译器支持Flutter的两个关键特性的组合：基于JIT(即时编译)的快速开发周期：允许使用类型的语言进行形状更改和有状态的热重载，Dart在 JIT模式下，速度与 JavaScript基本持平。 以及AOT(提前编译)编译器，可生成高效的ARM代码，可以快速启动并拥有可预测的生产部署性能。当以 AOT模式运行时，JavaScript便远远追不上了。
2. Dart可以更轻松地创建以60fps运行的流畅动画和转场
3. 快速内存分配。Flutter框架使用函数式流，它很大程度上依赖于底层的内存分配器，Dart可以在没有锁的情况下进行对象分配和垃圾回收。
4. 听说Dart和Flutter两个项目组挨着，不用Dart不好意思。官方说法是我们有机会与Dart社区密切合作，Dart社区正在积极投入资源改进Dart在Flutter中的使用。
5. Dart是**类型安全**的语言，拥有完善的包管理和诸多特性。
6. 开发人员发现Dart特别容易学习，因为它具有静态和动态语言用户都熟悉的特性。

## Flutter应用程序性能如何？

Flutter应用程序性能非常出色。Flutter旨在帮助开发人员轻松实现恒定的60fps。Flutter应用程序通过本机编译的代码运行 - 不涉及解释器。这意味着Flutter应用程序可以快速启动并执行。

## 热重载（Hot Reload）

Flutter可以热重载，保持当前状态，不用每次编译后都从首页进入到自己开发或者修改的界面。
几个地方不能热重载：
- 全局变量初始化器。
- 静态字段初始化程序。
- main()应用程序的方法

## 不使用原生控件

Flutter提供了一组自己的widget（包括Material Design和Cupertino（iOS风格的widget）），由Flutter的framework和引擎管理和渲染。从而得到更好的性能。
通过使用相同的渲染器、框架和一组widget，我们可以更轻松地同时发布iOS和Android应用，而无需执行仔细和昂贵的计划来维护两个独立的代码库。

## 一切皆为widget

- 一个结构元素（如按钮或菜单）
- 一个文本样式元素（如字体或颜色方案）
- 布局的一个方面（如填充）
- 等等…

而widget是不可变的，仅支持一帧，并且在每一帧上不会直接更新，要更新就必须使用Widget的状态。

## 部件有两种形式：无状态和有状态。

无状态部件在创建和初始化后不会更改它们的内容，而有状态部件维护一些程序运行时可变的状态，例如，响应用户交互。 无状态和有状态 widget 的核心特性是相同的，每一帧它们都会重新构建，有一个State对象，它可以跨帧存储状态数据并恢复它。

## 开发工具

Flutter 在开发工具的选择上很灵活。 应用程序可以通过命令行以及任何编辑器轻松开发，这些编辑器来自受支持的 IDE，如 VS Code，Android Studio 或 IntelliJ。 使用哪种 IDE 取决于用户的偏好。

**VS Code 提供了更轻松的开发体验**，因此它的启动速度往往比 Android Studio / IntelliJ 更快。

**Android Studio 提供了最多的功能。**例如 Flutter Inspector 来分析正在运行的应用程序的窗口部件以及监视应用程序性能。 还提供了开发部件层次结构时很方便的几个重构。

## 环境安装



由于在国内，需要配置下面两个环境变量

```
export PUB_HOSTED_URL=https://pub.flutter-io.cn
export FLUTTER_STORAGE_BASE_URL=https://storage.flutter-io.cn
```

变量名：PUB_HOSTED_URL，变量值：https://pub.flutter-io.cn



下载Flutter SDK的网址：https://flutter.io/sdk-archive/#windows



解压，在文件下找到flutter_console.bat，这个就是flutter命令行，运行flutter doctor检测(或者配置环境变量后直接在cmd上运行)：

![flutter_doctor1](/mdimage/flutter_doctor1.png)

![flutter_doctor2](/mdimage/flutter_doctor2.png)



## Android Studio安装

#### 环境：

1. Android Studio需要3.0或更高版本
2. Flutter支持的sdk环境：Android 4.1（API 16）或者更高版本。

#### 需要安装Flutter和Dart插件

- Flutter插件：支持Flutter开发工作流(运行、调试、热重载等)
- Dart插件：提供代码分析(输入代码时进行验证、代码补全等)

#### 安装上面两个插件的步骤:

1. 启动Android Studio.
2. 打开插件首选项 ( **Preferences>Plugins** on macOS, **File>Settings>Plugins** on Windows & Linux).
3. 选择 **Browse repositories…**, 选择 Flutter 插件并点击 install.
4. 重启Android Studio后插件生效.

#### 体验Flutter

定位到Android Studio 工具栏:

![control](/mdimage/control.png)

在 target selector 中, 选择一个运行该应用的Android设备. 如果没有列出可用，请选择 Tools>Android>AVD Manager 并在那里创建一个

体验热重载：修改代码后，按快捷键(Ctrl + s)或者点击闪电⚡图标，即可热重载



| 常用命令             | 含义                                    |
| -------------------- | --------------------------------------- |
| **--version**        | 查看Flutter版本                         |
| **-h**或者**--help** | 打印所有命令行用法信息                  |
| analyze              | 分析项目的Dart代码。                    |
| **build**            | Flutter构建命令。                       |
| channel              | 列表或开关Flutter通道。                 |
| clean                | 删除构建/目录。                         |
| config               | 配置Flutter设置。                       |
| **create**           | 创建一个新的Flutter项目。               |
| **devices**          | 列出所有连接的设备。                    |
| **doctor**           | 展示了有关安装工具的信息。              |
| drive                | 为当前项目运行Flutter驱动程序测试。     |
| format               | 格式一个或多个Dart文件。                |
| fuchsia_reload       | 在Fuchsia上进行热重载。                 |
| **help**             | 显示帮助信息的Flutter。                 |
| **install**          | 在附加设备上安装Flutter应用程序。       |
| **logs**             | 显示用于运行Flutter应用程序的日志输出。 |
| packages             | 命令用于管理Flutter包。                 |
| precache             | 填充了Flutter工具的二进制工件缓存。     |
| **run**              | 在附加设备上运行你的Flutter应用程序。   |
| screenshot           | 从一个连接的设备截图。                  |
| stop                 | 停止在附加设备上的Flutter应用。         |
| test                 | 对当前项目的Flutter单元测试。           |
| trace                | 开始并停止跟踪运行的Flutter应用程序。   |
| **upgrade**          | 升级你的Flutter副本。                   |