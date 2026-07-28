# 零基础个人 Portfolio 部署到 GitHub Pages 教程

这篇教程适合完全不会编程的读者。完成后，你会拥有一个任何人都能访问的个人网站，网址类似：

```text
https://你的GitHub用户名.github.io
```

GitHub Pages 是 GitHub 提供的免费静态网站托管服务。你不需要购买服务器，也不需要学习复杂的部署命令。

---

## 一、开始前需要准备什么

你需要：

- 一个可以正常收取邮件的邮箱
- 一台电脑
- 一个准备好的个人网站文件夹
- 稳定的网络连接

网站文件夹中至少要有一个名为 `index.html` 的文件。常见的网站文件如下：

```text
portfolio/
├── index.html
├── style.css
├── script.js
└── images/
    ├── avatar.jpg
    └── project-1.jpg
```

其中，`index.html` 是网站首页。它的名称必须完全一致，不能写成 `Index.html`、`index.htm` 或其他名字。

> 如果你还没有网站文件，可以先使用网页生成工具或 AI 工具制作一个静态个人网站，再按照本教程上传。

---

## 二、注册 GitHub 账号

### 1. 打开 GitHub

在浏览器中访问：

[https://github.com](https://github.com)

点击页面右上角的 **Sign up**。

### 2. 填写注册信息

按照页面提示填写：

1. **Email**：你的邮箱地址
2. **Password**：账号密码
3. **Username**：GitHub 用户名
4. 是否接收产品邮件

用户名非常重要，因为它会成为个人网站网址的一部分。

例如，你注册的用户名是：

```text
xiaoming
```

那么网站地址就是：

```text
https://xiaoming.github.io
```

选择用户名时建议：

- 使用英文、数字或短横线
- 尽量简短，方便别人记忆
- 避免频繁修改
- 不要使用空格或中文

### 3. 完成人机验证和邮箱验证

完成 GitHub 页面上的人机验证后，GitHub 会向你的邮箱发送验证码或验证邮件。

打开邮箱，按照邮件提示完成验证。验证完成后，登录 GitHub。

---

## 三、创建网站仓库

GitHub 中用来存放项目文件的地方叫作 **Repository**，中文通常称为“仓库”。

### 1. 新建仓库

登录 GitHub 后：

1. 点击右上角的 **+**
2. 点击 **New repository**

也可以直接打开：

[https://github.com/new](https://github.com/new)

### 2. 填写仓库信息

假设你的 GitHub 用户名是 `xiaoming`，那么 **Repository name** 必须填写：

```text
xiaoming.github.io
```

请把 `xiaoming` 替换成你自己的 GitHub 用户名。

需要特别注意：

- 用户名必须完全正确
- 后面必须是 `.github.io`
- 不要添加空格
- 建议全部使用小写字母

接着进行以下设置：

- **Description**：可以填写 `My personal portfolio`
- 选择 **Public**
- 可以勾选 **Add a README file**

最后点击 **Create repository**。

> 免费使用 GitHub Pages 时，最简单的方式是创建公开仓库。公开仓库中的文件所有人都能看到，因此不要上传密码、身份证照片、银行卡信息或其他隐私文件。

---

## 四、上传 Portfolio 网站文件

进入刚刚创建的仓库后：

1. 点击 **Add file**
2. 点击 **Upload files**
3. 将个人网站文件夹中的所有文件拖到上传区域

请上传文件夹里面的内容，而不是只上传最外层文件夹。

正确结构：

```text
xiaoming.github.io/
├── index.html
├── style.css
├── script.js
└── images/
```

容易出错的结构：

```text
xiaoming.github.io/
└── portfolio/
    ├── index.html
    └── style.css
```

在错误结构中，`index.html` 不在仓库最外层，打开网站时可能出现 404。

### 提交上传

文件上传完成后，向下滚动到 **Commit changes**：

1. 在标题中填写 `Upload portfolio website`
2. 点击绿色的 **Commit changes**

“Commit” 可以简单理解为“保存这次修改”。

> GitHub 网页上传不支持直接上传空文件夹。如果某个文件夹是空的，不需要上传。

---

## 五、开启 GitHub Pages

对于名称为 `你的用户名.github.io` 的仓库，GitHub 通常会自动部署网站。如果网站没有自动出现，可以手动检查：

1. 打开仓库
2. 点击顶部的 **Settings**
3. 在左侧菜单中点击 **Pages**
4. 找到 **Build and deployment**
5. 在 **Source** 中选择 **Deploy from a branch**
6. 在 **Branch** 中选择 `main`
7. 文件夹选择 `/(root)`
8. 点击 **Save**

等待 1～10 分钟后，访问：

```text
https://你的GitHub用户名.github.io
```

例如：

```text
https://xiaoming.github.io
```

第一次部署偶尔会需要更长时间。可以稍等几分钟后刷新页面。

---

## 六、检查部署是否成功

部署成功后，在仓库的 **Settings → Pages** 页面通常会看到类似提示：

```text
Your site is live at https://xiaoming.github.io
```

点击网址即可打开网站。

你也可以在仓库顶部点击 **Actions**，查看部署过程：

- 绿色对勾：部署成功
- 黄色圆点：正在部署
- 红色叉号：部署失败

---

## 七、以后如何更新网站

如果只修改少量文件，可以继续使用 GitHub 网页操作。

### 方法一：替换文件

1. 在仓库中打开旧文件
2. 点击右上角的删除按钮
3. 点击 **Commit changes**
4. 返回仓库首页
5. 点击 **Add file → Upload files**
6. 上传新文件
7. 再次点击 **Commit changes**

### 方法二：直接编辑文字

对于 `index.html` 等文本文件：

1. 点击文件名
2. 点击右上角的铅笔图标
3. 修改内容
4. 点击 **Commit changes**

提交后，GitHub 会自动重新部署。一般等待几分钟即可看到新版本。

如果页面看起来没有变化，可以尝试强制刷新：

- Mac：`Command + Shift + R`
- Windows：`Ctrl + F5`

---

## 八、常见问题

### 1. 打开网站显示 404

依次检查：

- 仓库名是否为 `你的用户名.github.io`
- `index.html` 是否位于仓库最外层
- `index.html` 的拼写和大小写是否正确
- 仓库是否设置为 **Public**
- **Settings → Pages** 中是否选择了 `main` 和 `/(root)`
- 是否已经等待几分钟

### 2. 网站有文字，但没有图片

常见原因是图片路径错误或文件名大小写不一致。

例如，代码中写的是：

```html
<img src="images/avatar.jpg" alt="个人头像">
```

那么仓库中必须存在：

```text
images/avatar.jpg
```

`avatar.jpg` 和 `Avatar.jpg` 在 GitHub 上是两个不同的文件名。

另外，不要使用电脑本地路径：

```text
/Users/yourname/Desktop/avatar.jpg
C:\Users\yourname\Desktop\avatar.jpg
```

这类路径只在你自己的电脑上有效，其他人无法访问。

### 3. 页面没有样式

检查 `index.html` 中引用的 CSS 文件名是否与仓库中的文件一致。

例如：

```html
<link rel="stylesheet" href="style.css">
```

仓库中就必须有一个名为 `style.css` 的文件。

### 4. 修改后网站没有更新

可以：

1. 打开仓库的 **Actions** 页面，确认部署已经完成
2. 等待几分钟
3. 强制刷新浏览器
4. 使用无痕窗口重新打开网站

### 5. 上传时提示文件太大

GitHub 网页不适合上传大型视频或超大图片。建议：

- 将图片压缩后再上传
- 把视频上传到 YouTube、Bilibili 或 Vimeo，再嵌入网站
- 单张图片尽量控制在 1 MB 以内
- 不要上传安装包、原始设计工程或无关文件

### 6. 仓库默认分支不是 `main`

在 **Settings → Pages** 中选择实际存在的分支即可。有些旧仓库的默认分支可能叫 `master`。

---

## 九、让 Portfolio 更专业

建议至少包含以下内容：

- 姓名和个人简介
- 清晰的个人照片或头像
- 技能介绍
- 2～6 个代表项目
- 每个项目的图片、介绍和你的贡献
- 简历下载链接
- 邮箱或其他联系方式
- GitHub、LinkedIn 等个人链接

发布前请检查：

- 手机和电脑上是否都能正常浏览
- 所有链接是否可以点击
- 图片是否能显示
- 是否存在错别字
- 是否泄露个人隐私
- 简历和联系方式是否为最新版本

---

## 十、可选：绑定自己的域名

如果你购买了自己的域名，例如：

```text
www.xiaoming.com
```

可以在仓库的 **Settings → Pages → Custom domain** 中填写该域名。

绑定自定义域名还需要在域名服务商后台修改 DNS 记录。不同服务商的页面差别较大，建议参考 GitHub 官方文档和域名服务商的说明。

官方文档：

[为 GitHub Pages 配置自定义域名](https://docs.github.com/zh/pages/configuring-a-custom-domain-for-your-github-pages-site)

如果你第一次部署网站，可以先使用免费的 `github.io` 地址，确认网站运行正常后再绑定域名。

---

## 十一、最简操作清单

如果你只想快速完成部署，请按照下面的顺序操作：

1. 注册并验证 GitHub 账号
2. 创建名为 `你的用户名.github.io` 的公开仓库
3. 确保网站首页名为 `index.html`
4. 将网站文件上传到仓库最外层
5. 点击 **Commit changes**
6. 在 **Settings → Pages** 中选择 `main` 和 `/(root)`
7. 等待几分钟
8. 打开 `https://你的用户名.github.io`

完成以上步骤后，你的个人 Portfolio 就已经发布到互联网上了。

