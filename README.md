# Hanfeng Wang — Academic Homepage

个人学术主页，面向 OpenReview 资料关联与研究成果展示。

网站地址（启用 GitHub Pages 后）：https://sogoodmm.github.io/

## 首次发布

1. 打开仓库 **Settings → Pages**。
2. **Build and deployment → Source** 选择 **Deploy from a branch**。
3. Branch 选择 **main**，目录选择 **/(root)**，点击 **Save**。
4. 等待 GitHub Pages 部署成功，再访问主页。
5. 将主页地址填写到 OpenReview 的个人主页字段；请保证 OpenReview 姓名、机构及注册邮箱与主页一致。

这是一个纯静态页面，无需安装依赖或执行构建。直接在浏览器打开 `index.html` 即可本地预览。

## 添加论文

在 GitHub 打开 `index.html`，点击铅笔按钮编辑，搜索 `<script id="PUBLICATION_DATA"`。

将下面的对象填入 `publications` 数组。多个对象用英文逗号分隔，所有示例字段请替换成真实信息；不要发布示例论文。

```json
{
  "title": "Your paper title",
  "authors": ["Hanfeng Wang", "Coauthor Name"],
  "year": 2027,
  "venue": "Conference or journal name",
  "selected": true,
  "image": "",
  "imageAlt": "Overview of the paper",
  "paper": "",
  "code": "",
  "project": "",
  "bibtex": ""
}
```

- `title`、数字格式的 `year` 为必填；论文按年份从新到旧排列。
- `authors` 为作者姓名数组，Hanfeng Wang 自动加粗；共同一作可写成 `Hanfeng Wang*`。
- `selected: true` 会将文章纳入 Selected 筛选。
- `paper`、`code`、`project` 填写公开的完整 HTTPS 链接；无链接时保留空字符串。
- 可将缩略图上传到 `assets/`，然后填写 `image`，例如 `assets/paper-2027.png`；没有图片时自动使用纯文本布局。
- `bibtex` 填写引文内容，换行使用 `\n`，内容中的双引号使用 `\"`。
- JSON 不允许注释或尾随逗号；请保留英文双引号。文本中不要直接插入 HTML 或脚本结束标签。

提交更新后，GitHub Pages 会自动重新部署。

## 头像及学术链接

同一个 `PUBLICATION_DATA` 配置内：

- `profileImage`：头像路径，例如 `assets/avatar.jpg`；未填写时显示姓名缩写。
- `openreview`：自己的 OpenReview 个人主页完整链接。
- `scholar`：自己的 Google Scholar 个人主页完整链接。

未填写的学术链接不会显示。请勿使用其他人的身份链接。

## 内容与样式

个人简介、教育经历和邮箱直接写在 HTML 中，即使浏览器关闭 JavaScript 也可阅读。CSS 位于文件顶部的 `<style>` 内；论文渲染脚本位于底部。页面支持手机布局、键盘导航及减少动画偏好。

请勿向仓库提交密码、访问令牌或其他凭据。
