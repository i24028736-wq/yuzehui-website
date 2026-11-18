# Maison Serein 课堂演示练习

这是一份练习提纲，可根据自己的真实设计过程和课程 AI 披露规则调整。网站内容为英文；下列中文提示帮助准备口头讲解，英文句子可作为练习参考，不必逐字背诵。

## 演示前

1. 将整个 `restaurant` 文件夹保留在一起，打开其中的 `index.html`；用编辑器打开 `index.html` 和 `style.css`。
2. 打开 `home-wireframe.svg`，确认它是首页结构示意，不是成品截图。`README.md` 包含完整设计说明和媒体来源。
3. 页面、图片和视频均在本地，来源链接需要联网。视频使用浏览器播放，播放前可确认音量。联系表单为演示用途，不会发送或保存数据。
4. 如果准备现场改代码，先复制一份项目练习，或记下原值。每次改完保存并刷新，讲解后恢复原值。

## 约 2 分钟讲解顺序

1. **品牌与受众：**“This is Maison Serein, a fictional restaurant for young adults and couples who enjoy a relaxed evening and thoughtful food.”
2. **首页与线框图：** 展示线框图，再切回首页。指出桌面版左右两栏，手机端依次排列。“The homepage pairs a quiet headline with a candlelit table. The button links to the menu on the same page.” 点击 **Explore the menu**。
3. **菜单与图文关系：** 指出三道菜的图片、名称、说明和示例价格。“Each dish groups its image, name, description and price so visitors can scan it easily.” 菜品和价格是虚构示例。
4. **体验与视频：** 点击 **Experience** 并播放。“The page also includes a short cooking video. It is an independently sourced film, not footage of the fictional restaurant.” 影片为制作 pilaf；作者和许可列在视频下方和 README 中。
5. **联系与限制：** 点击 **Contact**。“The labels identify each field, and the disabled button makes it clear this is a demonstration form.” 联系方式均为虚构。
6. **设计原则与响应式：**“Contrast separates text from its background; repeated colours and type create consistency; shared edges give alignment; related details are grouped together.” 缩窄浏览器，展示导航换行、图片和内容纵向排列。
7. **素材说明：** 图片来自 Pexels；视频来自 Wikimedia Commons，作者及许可见 `README.md`。网页内容和设计说明基于虚构品牌。

## 四个现场修改练习

在项目副本中进行，修改后保存并刷新。最后恢复原值；以下示例均使用已存在的文件和目标。

1. **颜色：** 在 `style.css` 顶部将 `--cream:#f5f0e8` 改为 `--cream:#fff8ef`。观察背景；恢复为 `#f5f0e8`。
2. **标题：** 在 `index.html` 找到 `A little longer`，暂改为 `Stay a little longer`，保留 `<br>` 和 `<i>` 标签。观察标题换行；恢复原文。
3. **图片：** 找到首页的 `src="images/hero.jpg"`，暂改为已存在的 `src="images/about.jpg"`。同时把旁边 `alt` 暂改为 `A warmly lit restaurant table with candles and greenery`。刷新观察裁切；恢复原路径和原 alt。正式替换图片时应更新来源及许可记录。
4. **导航：** 将页头中的 `<a href="#menu">The menu</a>` 暂改为 `<a href="#contact">Contact</a>`，点击检查页面跳到 Contact；恢复原代码。解释 `href` 的 `#contact` 要与目标元素的 `id="contact"` 一致。

如果修改后效果不符合预期，先检查是否保存、是否刷新，以及引号、尖括号和文件路径是否完整。
