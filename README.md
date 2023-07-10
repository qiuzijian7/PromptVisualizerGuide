# PromptVisualizerGuide

## PromptVisualizer | 可视化提示词库 | 支持Notion提示词库自定义 

<p align="center">
    <img width="1430" src="https://github.com/qiuzijian7/PromptVisualizerGuide/assets/7805317/71f7f0d1-ca5f-42ca-8490-ffb9534f2e7b">
</p>

[**工具地址** www.promptvisualizer.com](https://www.promptvisualizer.com)

特性：
-   提示词可视化显示
-   提供chrome插件支持从Midjourney、PromptHero资源库中爬取图片和关键词保存到Notion中
-   支持从Notion中导入自定义预设
-   提示词自动翻译
-   多工作页签支持

## 使用教程

<a href="https://www.bilibili.com/video/BV15N411P7D3/?spm_id_from=333.337.search-card.all.click&vd_source=1f6edbc8e03c44932da52d02c0c11c1c" target="_blank">
 <img width="300" src="https://user-images.githubusercontent.com/82231420/230757939-dde301f1-bf68-4455-83c6-f7dd2214c68b.png">
</a>

[📺 B 站视频教程](https://www.bilibili.com/video/BV15N411P7D3/?spm_id_from=333.337.search-card.all.click&vd_source=1f6edbc8e03c44932da52d02c0c11c1c)


## 如何连接的我的 Notion 来管理自己的词典

 支持使用 [Notion](https://www.notion.so/) 来管理自己的词典，使用 Notion 管理相对简单，可自定义程度也很高。

### 1. 复制「PromptVisualizer预设收集」

复制我们的模板文档到你自己的 Notion 工作区中

[**📕 PromptVisualizer预设收集**](![](https://working-uncle-0b5.notion.site/da1ab037fdc6427eaa17719a7af3e0bf?v=a418c640b3fe4f498f2f91e2a318e6e2))

![](https://github.com/qiuzijian7/PromptVisualizerGuide/assets/7805317/e94a96e6-bfdd-4b9d-a89a-d4e11579a916)


表头说明： `Platfrom`, `Tags`、`WebLink`、`Prompt`、`NegativePrompt`、`translation`、`Property`、`UserName`、`Images`、`ImageFile` *不要变更表头*

#### Notion 表头定义

| 表头       | 作用                                                    |
| -------    | ------------------------------------------------------- |
| Platfrom   | 提示词应用平台                            |
| Tags       | 分类标签                                        |
| WebLink | 源地址链接 |
| NegativePrompt     | 负面词，有些平台如stable diffusion有负面词功能      |
| translation   | 翻译                            |
| Property   | 命令                            |
| UserName   | 作者名称                            |
| Images   | AI图片URL                            |
| ImageFile   | AI图片资源，有些平台有URL防盗链接（如PromptHero），无法通过URL显示图片，因此可将图片下载下来后手动上传到IamgeFile列中。（Notion API不允许通过API自动上传）                            |

### 2. 创建自己的 Notion 集成插件（integrations）

要让 Prompt Visualizer 连接到自己的 Notion 数据库，需要创建一个自己的集成（integrations）。Prompt Visualizer 根据生成的token连接到你的数据库。

#### 2.1 打开集成开发页面

打开 Notion 的集成开发页面 [🔗 www.notion.so/my-integrations](https://www.notion.so/my-integrations)
点击 「+ new integrations」按钮创建一个新集成插件

![20230710-102720](https://github.com/qiuzijian7/PromptVisualizerGuide/assets/7805317/ce6d34a4-eec4-4a44-91af-6dc14da554f3)



#### 2.2 创建集成插件

创建intergration，任意命名，如MyPromptVisualizer

![20230710-102724](https://github.com/qiuzijian7/PromptVisualizerGuide/assets/7805317/b7a012e0-b2a5-4901-ab3d-1c3220e9939e)


#### 2.3 获取集成插件 Token 密钥

集成插件创建完毕后，复制 Token 秘钥保存下来，你将使用此 Token 作为访问凭证，请妥善保管不要在公开场合泄露。

![](https://github.com/qiuzijian7/PromptVisualizerGuide/assets/7805317/a39ebc6d-7c80-4362-bbf2-7927f2fd5638)
#### 2.4 获取数据库web link

将你自己工作区中的[PromptVisualizer预设收集]网页地址复制保存下来
![](https://github.com/qiuzijian7/PromptVisualizerGuide/assets/7805317/3f4c3bde-1dce-433b-818c-89067ea92d47)


#### 2.5 在数据库页面链接到你的集成

集成插件创建后，还需要在你的 Notion 数据库的菜单中连接到你的集成插件：
![](https://github.com/qiuzijian7/PromptVisualizerGuide/assets/7805317/90844f4c-e382-44b4-a873-d52dfd4d2de0)


### 3. Prompt Visualizer配置 Notion
#### 3.1 Prompt Visualizer chrome插件中配置
- 安装Prompt Visualizer Plgin
- 插件中打开SettingPage->配置Key和Page地址->最后点保存

![](https://github.com/qiuzijian7/PromptVisualizerGuide/assets/7805317/0355518c-d432-4520-8a7c-505eb0238c04)

![20230710-102744](https://github.com/qiuzijian7/PromptVisualizerGuide/assets/7805317/cdf0cdda-86c0-458e-98e6-042f11ffa7fc)

- AI网站中鼠标右键点击“Save to Notion”，Notion中会自动增加该提示词

![](https://github.com/qiuzijian7/PromptVisualizerGuide/assets/7805317/2c0cc6eb-b0e2-48c4-9678-89ba92862817)

![](https://github.com/qiuzijian7/PromptVisualizerGuide/assets/7805317/243f89d6-9b42-4f98-993d-4edde3e4b581)

#### 3.2 Prompt Visualizer web工具中配置
- 打开网站[Prompt Visualizer](https://www.promptvisualizer.com/)网站
- 打开右上角输入key和notion的weblink（参见2.3和2.4）
![](https://github.com/qiuzijian7/PromptVisualizerGuide/assets/7805317/cfb84917-7fa2-4b19-85e7-8c4ac79103e8)
- 点击载入后，查看prefab效果如下：
![](https://github.com/qiuzijian7/PromptVisualizerGuide/assets/7805317/6d419bf5-1d2d-4cf1-9d6a-e10c9c69465a)



