# ViTacDex 网站上传包

这是可独立部署的静态网站，沿用原 `index.html` 模板的布局和样式。
网页、视频、图片、论文、字体、图标和 JavaScript 均包含在此目录中。
无需 npm、构建步骤、Python 服务或外部 CDN。

## 上传到 GitHub Pages

1. 将本目录中的**全部内容**上传至你的 GitHub 仓库根目录，保持 `static` 下的目录结构。
2. 仓库根目录应直接出现 `index.html` 和 `static/`，不要只上传 `index.html`，也不要只上传 ZIP 文件。
3. 打开仓库 **Settings → Pages**。
4. 在 **Build and deployment → Source** 选择 **Deploy from a branch**。
5. 选择存放文件的分支（通常是 `main`）和 **/(root)**，点击 **Save**。
6. 等待 GitHub 显示网站地址后，通过该地址访问。仓库文件浏览页面不是网站播放页面。

这些配置步骤依据 [GitHub Pages 官方文档](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site)。

请一并保留 `.nojekyll`。ZIP 是传输和备份包，上传网站前应先解压。
外部作者主页、相关研究链接及模板许可链接仍指向各自网站；页面显示和视频播放不依赖这些链接。

## 文件结构和引用

```text
index.html                         网站入口
.nojekyll                          直接发布静态文件
.gitattributes                     文本与二进制文件类型
static/
  css/                             模板样式和本地字体声明
  js/                              jQuery、图标、Bulma 组件与页面脚本
  fonts/                           原模板使用的本地字体
  webfonts/                        Font Awesome 图标字体
  images/vitacdex/                 论文图表、视频预览图
  videos/vitacdex/                 网页所用 MP4 视频及保留的原展示视频
  papers/vitacdex.pdf              ViTacDex 论文
asset-manifest.json                文件大小、SHA-256 和引用关系
THIRD_PARTY_NOTICES.md              外部库和字体来源
```

所有网页资源均采用相对路径（如 `./static/videos/vitacdex/demo-x.mp4`），可用于用户主页仓库，也可用于带仓库子路径的项目网站。不要改变文件名大小写，不要把视频路径改成本机盘符或 `127.0.0.1`。

## 视频对应关系

| 文件 | 页面用途 |
| --- | --- |
| `hero.mp4` | 首页背景视频 |
| `overview.mp4` | Abstract 后的概览视频 |
| `demo-x.mp4` | −X 轴实验：原视频、球形点云、四指触觉 |
| `demo-z.mp4` | Z 轴实验：原视频、球形点云、四指触觉 |
| `comparison.mp4` | 传感模态对比 |
| `diverse-objects.mp4` | 原拼接视频，已从页面移除以避免重复 |
| `additional-objects.mp4` | 原拼接视频，已从页面移除以避免重复 |
| `occlusion.mp4` | 局部视觉遮挡 |
| `random-occlusion.mp4` | 间歇视觉遮挡 |
| `clutter.mp4` | 背景视觉干扰 |
| `supplementary.mp4` | 原补充视频，已从页面移除 |
| `mixed-*.mp4` | Mixed Demonstration，6 个独立实验 |
| `difficult-*.mp4` | Difficult-to-Grasp Shapes，4 个实验 |
| `symmetrical-object.mp4`、`transparent-object.mp4` | 对称及透明物体，2 个实验 |

视频为供网页播放的 H.264 MP4 副本；原始实验文件没有修改。
每个视频已完整解码检查。字体、图标、样式、脚本、图片和论文链接也已检查。

## 在本机查看

可双击本目录的 `index.html`。视频默认静音；若浏览器阻止自动播放，可点击播放器播放。
此前的 `http://127.0.0.1:8767/` 是临时本地预览地址，不是部署地址，也不用于此上传包的任何引用。

## 内容来源

科学内容、作者、方法图和结果表来自提供的 ViTacDex 论文草稿。视频来自提供的实验记录、补充视频及从 PPT 提取的原始视频。
页面保留原 TactileLab / Nerfies 模板结构及其署名；未加入未提供的 arXiv 编号、代码仓库或录用信息。
