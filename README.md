# AI 科研新手破局

这是一个本地 HTML 幻灯片项目，主题是“从零起步到顶会投稿”的 AI 科研入门路径。内容覆盖文献检索与阅读、选题定位、代码复现、论文写作、投稿、rebuttal 和拒稿修稿。

演示文稿的标题页信息为：陈国瑞，2026-08-24，GuoRuiC@outlook.com。

## 快速开始

直接用浏览器打开 [AI科研新手破局.html](./AI科研新手破局.html) 即可播放。

如果浏览器限制了本地资源加载，可以在当前目录启动一个临时静态服务器：

```powershell
python -m http.server 8000
```

然后访问 <http://localhost:8000/AI科研新手破局.html>。

## 播放控制

| 按键 | 功能 |
| --- | --- |
| `←` `→`、`Space` | 上一页 / 下一页 |
| `PgUp` `PgDn` | 上一页 / 下一页 |
| `Home` `End` | 跳到第一页 / 最后一页 |
| `F` | 全屏 |
| `S` | 打开演讲者模式（当前页、下一页、讲稿和计时器） |
| `N` | 打开或关闭当前页备注 |
| `O` | 打开幻灯片总览 |
| `T` | 切换主题 |
| `A` | 播放当前页的演示动画 |

## 文件结构

```text
.
├── AI科研新手破局.html       # 幻灯片正文、备注和页面结构
├── AI科研新手破局.css        # 本演示文稿的专属样式
├── ai-research-ppt-images/   # 演示文稿使用的图片和 SVG 素材
├── html-ppt-assets/          # 通用字体、基础样式、主题和动画运行时
│   ├── themes/               # 可切换的主题 CSS
│   └── animations/           # CSS 动画和 Canvas 动效
└── .tmp/html-ppt-skill-main/ # HTML PPT 工具的本地参考副本
```

## 修改方式

- 修改页面内容、讲稿或页序：编辑 `AI科研新手破局.html`。
- 修改本演示文稿的颜色、间距和布局：编辑 `AI科研新手破局.css`。
- 替换图片：将文件放入 `ai-research-ppt-images/`，并同步修改 HTML 中对应的 `src`。
- 切换默认主题：修改 HTML `<head>` 中 `theme-link` 的主题文件路径，例如 `html-ppt-assets/themes/academic-paper.css`。
- 页面备注位于每页的 `<aside class="notes">` 中；按 `S` 可在演讲者模式中查看。

## 说明

这是一个无需构建步骤的纯静态项目。`html-ppt-assets/` 中的运行时负责翻页、主题切换、总览、全屏和演讲者模式；`.tmp/html-ppt-skill-main/` 仅用于保存生成这套资源时所参考的 HTML PPT 工具文件，播放演示文稿不依赖它。

