---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
---
# 数字化资源 物理

## 上课汇报的内容

### 选题思路

在高中物理课程中，曲线运动是一个非常重要的主题，它涉及到许多基本的物理概念和数学技能，对学生理解运动学和动力学有着重要的影响。以下是曲线运动在高中物理中的重要性：

1. **理解位移、速度和加速度**：通过研究曲线运动，学生可以更深入地理解位移、速度和加速度的概念。曲线运动可以帮助他们理解这些量是如何随时间变化的，并且如何在不同类型的运动中相互关联。
2. **应用微积分**：曲线运动的研究涉及到对曲线的切线、曲率等概念，这些概念需要用到微积分中的导数和积分。因此，通过曲线运动的学习，学生可以初步接触到微积分的概念和应用。
3. **理解力学原理**：曲线运动的研究可以帮助学生理解牛顿运动定律在复杂运动情况下的应用。例如，当物体沿着曲线运动时，如何分解力的分量，以及如何应用牛顿第二定律来分析曲线运动中的物体。
4. **应用向心力和离心力**：曲线运动的学习可以帮助学生理解向心力和离心力的概念。这些力在圆周运动和其他曲线运动中起着至关重要的作用，通过学习曲线运动，学生可以更好地理解这些力对物体运动轨迹的影响。
5. **实际应用**：曲线运动的理解对于许多实际情况都非常重要，比如汽车在转弯时的运动、天体运动的轨迹等。通过学习曲线运动，学生可以将物理原理应用到日常生活和其他科学领域中。

因此，曲线运动在高中物理课程中的重要性不仅在于它本身是一个重要的物理概念，更在于它对学生理解物理学和数学的整体框架有着重要的影响。

### 设计思路

考虑到主流的html直接写过于复杂，我们采用先编写markdown语言的方式，再将Jekyll站点部署到Azure Static Web应用
> [Jekyll](https://jekyllcn.com/docs/home/) 是一个简单的博客形态的静态站点生产机器。它有一个模版目录，其中包含原始文本格式的文档，通过一个转换器（如 [Markdown]）和我们的 Liquid 渲染器转化成一个完整的可发布的静态网站，你可以发布在任何你喜爱的服务器上。Jekyll 也可以运行在 GitHub Page 上，也就是说，你可以使用 GitHub 的服务来搭建你的项目页面、博客或者网站，而且是完全免费的。
> > [Markdown](https://markdown.com.cn/basic-syntax/)是一种轻量级标记语言，排版语法简洁，让人们更多地关注内容本身而非排版。它使用易读易写的纯文本格式编写文档，可与HTML混编，可导出 HTML、PDF 以及本身的 .md 格式的文件。因简洁、高效、易读、易写，Markdown被大量使用，如Github、Wikipedia、简书等。
> 
> > [HTML](https://developer.mozilla.org/zh-CN/docs/Learn/Getting_started_with_the_web/HTML_basics)不是一门编程语言，而是一种用于定义内容结构的标记语言。HTML 由一系列的元素组成，这些元素可以用来包围不同部分的内容，使其以某种方式呈现或者工作。一对标签可以为一段文字或者一张图片添加超链接，将文字设置为斜体，改变字号，等等。例如，键入下面一行内容：

>Azure 云平台汇集的产品和云服务超过 200 种，旨在帮助你将新解决方案付诸实践，以便解决当今的难题，并创造未来。利用所选的工具和框架，在多个云中、在本地以及在边缘生成、运行和管理应用程序.

#### 先决条件
1. 安装 Jekyll
2. 如有必要，可使用适用于 Linux 的 Windows 子系统并按照 Ubuntu 说明操作。
3. 具有活动订阅的 Azure 帐户。 如果没有帐户，可以免费创建一个帐户。
4.  一个 GitHub 帐户。 如果没有帐户，可以免费创建一个帐户。
5.   已安装 Git 安装程序。 如果没有 Git，则可以安装 Git。

#### 创建 Jekyll 应用

使用 Jekyll 命令行接口 (CLI) 创建 Jekyll 应用：

1.从终端运行 Jekyll CLI 来创建一个新的应用。

> A terminal emulator is a program that allows the use of the terminal in a graphical environment. As most people use an OS with a graphical user interface (GUI) for their day-to-day computer needs, the use of a terminal emulator is a necessity for most Linux server users.

Here are some free, commonly-used terminal emulators by operating system:

    Mac OS X: Terminal (default), iTerm 2
    Windows: ConEmu, Windows Terminal, PuTTy
    Linux: Gnome Terminal, Konsole, XTerm


```Bash
jekyll new static-app
```

2. 转到新建的应用。

```Bash
cd static-app
```

3. 初始化新的 Git 存储库。

> Git is a fast, scalable, distributed revision control system with an unusually rich command set that provides both high-level operations and full access to internals.

```Bash
 git init
```

4. 提交更改。

```Bash
git add -A
git commit -m "initial commit"
```

#### 将应用程序推送到 GitHub

Azure 静态 Web 应用使用 GitHub 来发布你的网站。 以下步骤展示了如何创建 GitHub 存储库。

1. 从 https://github.com/new 创建一个名为 jekyll-azure-static 的空白 GitHub 存储库（不创建自述文件）。
   
2. 将 GitHub 存储库作为远程存储库添加到本地存储库。 确保添加 GitHub 用户名，来替代下面命令中的 <YOUR_USER_NAME> 占位符。
```Bash 

git remote add origin https://github.com/<YOUR_USER_NAME>/jekyll-azure-static
```

3. 将本地存储库推送到 GitHub。
```Bash

    git push --set-upstream origin main
```
> 备注
> 你的 git 分支的命名方式可能与`main`不同。 用正确的值代替此命令中的`main`

#### 部署 Web 应用

下列步骤说明了如何创建新的静态站点应用并将其部署到生产环境。
创建应用程序

1. 转到 Azure 门户
   
2. 选择“创建资源”
   
3. 搜索“静态 Web 应用”
   
4. 选择“Static Web Apps”
   
5. 选择“创建”
   
6. 在“基本信息”选项卡上，输入下列值。

|属性 |	值|
|-------| ----- |
|订阅 	|Azure 订阅名称|
|资源组 |	jekyll-static-app|
|名称 |	jekyll-static-app|
|计划类型 |	免费|
|Azure Functions API 和过渡环境的区域 	|选择离你最近的区域。|
|Source |	GitHub|

7. 选择“使用 GitHub 登录”，然后向 GitHub 进行身份验证。

8. 输入以下 GitHub 值。

    | 属性 | 值   |
    | ---- | ---- |
    |组织 	|选择所需的 GitHub 组织。|
    |存储库 |	选择“jekyll-static-app”。|
    |分支 	|选择“主要”。|
    

> 如果看不到任何存储库，则可能需要在 GitHub 中授权 Azure Static Web Apps。 浏览到 GitHub 存储库，转到“设置”>“应用程序”>“授权 OAuth 应用”，选择“Azure Static Web Apps”，然后选择“授予”。 对于组织存储库，你必须是组织的所有者才能授予权限。

9.  在“生成详细信息”部分，从“生成预设”下拉列表中选择“自定义”，并保留默认值。
    
  10. 在“应用位置”框中输入“./”。
    
   11.  将“API 位置”框留空。
    
   12.  在“输出位置”框中，输入“_site”。

#### 查看并创建

   1. 选择“查看 + 创建”，以验证详细信息是否全部正确。
    
   2. 选择“创建”，开始创建应用服务静态 Web 应用并为部署预配 GitHub Actions。
    
3.    部署完成后，请选择“转到资源”。
    
  4.  在资源屏幕上，选择 URL 链接，以打开已部署的应用程序。 你可能需要等待一两分钟，GitHub Actions 才能完成。

### 组内具体分工

|学号	|姓名	|分工|
|---|---|——-|
|07200425|陈奕|整理技术文档内容，统筹项目方向与进度|
|||负责编写网站中的物理知识内容，包括曲线运动的相关理论|
|||确保网站内容符合高中物理教学大纲要求，具有教育性和可理解性|
|||负责梳理这几年来的模考题和高考相关题目，揣摩主要的考查方式|
|||确保网站在不同设备上都有良好的显示效果，并具备良好的用户交互体验|
|||负责对物理知识内容进行文案编辑，确保语言表达准确清晰|


### 评价量表维度的建议

1. 考虑互动性和反馈效果。

> 提倡评价应关注学生的个体差异，帮助学生认识自我、建立自信，改进学习方式，发展核心素养——《普通高中物理课程标准（2017年版2020年修订）》

1. 网站观看效果的监测。（视频完播率，点击率，测试小题目）

>  各学科明确学生完成本学科学习任务后，学科核心素养应该达到的水平，各水平的关键表现构成评价学业
> 质量的标准。——《普通高中物理课程标准（2017年版2020年修订）》
