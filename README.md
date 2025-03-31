# Github 页面图库
使用 Thumbsup 和 Github Actions 免费轻松地在 Github 页面上托管您的照片/视频库。

### 为什么要这个项目？
该项目包含入门代码，适用于想要在 Github Pages 上部署其照片/视频库的任何人，
**无需任何编码**。由于 Github pages 是 Github 提供的免费托管服务，用于托管静态页面，因此
提供不错的带宽。因此，对于摄影师来说，这是一个展示作品的绝佳选择。Github Actions 是一个 CI & CD
为开源项目提供无限构建的平台。将 GitHub 页面的强大功能与 Github Actions 结合起来，
一个零美元的解决方案，让您的画廊在线。

### 如何使用
按照以下步骤将您的 Gallery 联机。您将使用 GitHub 网页界面完成所有操作。
:wink: 没有令人沮丧的 CLI：
1. 注册 Github 账户并验证你的邮箱地址：https://github.com/join
2. 点击使用此模板按钮：

![template](https://user-images.githubusercontent.com/8397274/103133407-40d86f00-46d0-11eb-82f2-edb4a0a30333.png) 

3. 为你的新仓库输入一个名称

![name](https://user-images.githubusercontent.com/8397274/103133448-88f79180-46d0-11eb-87ee-8da7a7d63473.png) 

4. 点击设置选项卡。点击 **代码和自动化** 部分下的 **页面** 选项。确保你已选择 **GitHub 操作** 作为 GitHub 页面的 **来源**。
   ![Pages](https://user-images.githubusercontent.com/8397274/222885316-edd4dad3-fcdd-4c23-ad3a-dd96fa8bc426.png) 

5. 点击您帐户下新创建的存储库中的编辑按钮来编辑 [config.json](config.json)：

```
{
  “输入”：“。/画廊”，
  “输出”：“。/build_output”，
  "title": "照片库",// 在此设置您的图库标题
  "sort-albums-by": "标题",
  "sort-media-by": "文件名",
  "下载照片": "复制",
  “清理”：真，
  "theme": "cards", // 你的主题
  “css”：“。/custom.css”，
  “footer”：“版权文本”，//在此设置您的版权文本
  “使用情况统计”：false
}
```
您可以从以下任意主题中选择来设置主题键的值：
* `mosaic` - https://thumbsup.github.io/demos/themes/mosaic/
* `卡片` - https://thumbsup.github.io/demos/themes/cards/
* `经典` - https://thumbsup.github.io/demos/themes/classic/
* `flow` - https://thumbsup.github.io/docs/4-themes/built-in/ (无可用演示)

您可以在此处了解有关配置文件的更多信息：https://thumbsup.github.io/docs/3-configuration/usage/。单击页面下方的提交更改按钮。

6. 转到新存储库的操作选项卡，等到初始构建完成。它将显示以下复选标记：
![操作](https://user-images.githubusercontent.com/8397274/103133265-7af54100-46cf-11eb-9cef-38fa122142aa.png)
7. 您已设置好新的精彩图库！添加相册或照片即可让其上线。

#### 演示视频
[![demo](http://img.youtube.com/vi/uYh7b2V0pyA/0.jpg)](http://www.youtube.com/watch?v=uYh7b2V0pyA "Github 页面图库演示")


#### 将新相册添加到画廊
1. 进入分叉 repo 的画廊文件夹。
2. 单击创建新文件按钮。
3.在输入框中输入AlbumName/.gitkeep
4. 点击底部的提交更改按钮。

![newfolder](https://media.giphy.com/media/455paOHOAWr4KWNOtg/giphy.gif) 

#### 添加媒体
1. 进入图库文件夹。如果有相册，请打开。
2. 点击上传文件按钮
3. 选择文件。上传完成后，点击提交更改按钮。

![selectmedia](https://media.giphy.com/media/2uIfenjYx5anbQOEAo/giphy.gif) 

#### 查找您的网站网址
如果你已完成上述所有步骤，那么你的网站现在就可以上线了。请查看你的存储库中的 Github Actions 选项卡，了解
部署。完成后，再次转到设置选项卡并向下滚动到 Github Pages 部分以找到您的公共画廊 URL。

![url](https://user-images.githubusercontent.com/8397274/48008065-f639b880-e13e-11e8-9f8e-72d27ad7cc30.png) 

## 限制
* Github Pages [服务条款](https://help.github.com/articles/github-terms-of-service/):
> 如果您的带宽使用量明显超过其他 GitHub 客户的平均带宽使用量（由 GitHub 独自决定），我们保留立即禁用您的帐户或限制您的文件托管的权利，直到您可以减少带宽消耗为止。

* 文件大小限制（100 MB）和 Repo 大小限制（75 GB）和上传限制（25MB）：Github 将所有文件的最大可用文件大小限制为 100MB。这对大多数用户来说已经足够了。它还规定了 75GB 的 repo 大小限制。如果您通过浏览器将文件添加到存储库，则文件不能大于 25 MB。请访问 https://help.github.com/articles/what-is-my-disk-quota/ 了解更多信息。


使用的工具
* [Github Actions](https://github.com/features/actions) 用于持续部署。
* [Thumbsup](https://thumbsup.github.io/) 用于生成图库静态页面。
* [GithHub Pages](https://pages.github.com/) 用于托管。

### 历史记录
* 该项目最初使用 Travis CI，为了提高速度和可靠性，已迁移到 Github Actions。Travis 停止为开源项目提供免费的无限构建。

## 贡献
请随意进行任何更改并提交 PR。
