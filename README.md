# Cool Papers

Immersive Paper Discovery（沉浸式刷论文！）

这里记录Cool Papers的更新日志，并且收集用户的反馈和建议。

## 链接
- **Cool Papers**: [https://papers.cool](https://papers.cool)
- **Kimi Chat**: [https://kimi.moonshot.cn](https://kimi.moonshot.cn/?ref=papers.cool)
- **科学空间博客**: [https://kexue.fm](https://kexue.fm)

## 更新

### 2024.01.20
- **PDF抽取文本优化**：进一步优化PDF抽取文本的效果，理论上Kimi的FAQ质量会有所提升；
- **搜索字段加入作者**：Bar上的页面内搜索字段增加作者，并且目前按浏览器页面内搜索的快捷键（CMD+F or CTRL+F）会自动弹出自行编写的搜索。

### 2024.01.18
- **列表页延时加载**：论文列表引入延时加载功能，提高列表数量过多时的加载速度，当以正常速度进行阅读的情况下，延时加载基本上是无感的。

### 2024.01.17
- **页面搜索支持反选**：优化页面内搜索，同时支持包含某些关键词以及排除某些关键词。

### 2024.01.16
- **Arxiv更新优化**：优化获取Arxiv最新论文列表的逻辑，理论上论文更新将会更稳定、更及时；
- **支持导出阅读记录**：点击列表页下方的Bar中间的星星，就会出现点击过[PDF]或者[Kimi]的论文列表，点击“Export”就会打开一个只包含这些论文的新页面，复制这个新页面的链接地址，就可以在其他设备或者与其他人分享阅读记录。

### 2024.01.15
- **论文更新滞后**：今天Cool Papers在下午三点之后才更新，这是因为[官方Blog](https://blog.arxiv.org/2024/01/10/attention-authors-temporary-change-to-announcement-schedule-due-to-mlk-jr-holiday/)发布了今天不更新的公告，所以站长主动跳过了今天的更新，直到有用户提醒，才发现原来今天Arxiv是有更新的；
- **适配早年论文Id**：此前Cool Papers适配的Arxiv ID为“\d{4}\.\d{5}”的格式，即四位年月加五位编号，后来发现早年的Arxiv ID有“\d{4}\.\d{4}”的格式，如Word2Vec是[1301.3781](https://papers.cool/arxiv/1301.3781)、GAN是[1406.2661](https://papers.cool/arxiv/1406.2661)，对此类情况做了适配和重定向（比如1406.2661其实访问1406.02661也可以，同理2401.06769访问2401.6769也可，会重定向到同一篇论文），为以后可能开放所有历史论文做准备；
- **其他兼容性拓展**：未来可能会进一步引入Arxiv以外的论文源，所以对页面模版等细节做了进一步泛化，这部分更新对用户来说基本无感。

### 2024.01.09
- **支持历史日期列表**：应很多用户请求，开通历史日期论文列表访问支持，可以在首页通过日历图标选择日期。这个历史列表是基于Cool Papers本身的累积，而不是实时从Arxiv获取（Arxiv也不支持访问一周以前的历史列表），所以目前的数据有限，再加上此前刚开发时有过一段数据混乱期，所以只支持2024年开始的日期。

### 2024.01.08
列表页底部加了个Bar，支持一些快捷操作：
- **回到首页**：跳转回网站首页；
- **页面搜索**：支持多个关键词高亮，支持只显示匹配上的论文；
- **星标列表**：显示页面内点击过[PDF]或者[Kimi]的论文列表；
- **魔法令牌**：输入Magic Token，解锁某些隐藏能力（暂不开放）；
- **问题反馈**：链接到本项目。

### 2024.01.04
- **更好的PDF预览效果**：更换[PDF.js](https://mozilla.github.io/pdf.js/)来加载PDF，可以获得更好的阅读效果，并且支持移动端浏览器加载（此前大部分移动端浏览器会触发下载PDF而不是预览PDF）。

### 2024.01.03
- **Arxiv论文列表混乱**：当某个分类下最新一天的论文数量少于25篇时，会把更早的文章混在当天文章列表中显示出来，通过[PyQuery](https://pyquery.readthedocs.io/en/latest/)实现更精准的html定位解决此问题。

### 2024.01.02
- **[Copy]导致选区混乱**：用户发现，当使用浏览器的页面查找时，如果同时点击[Copy]，那么会导致查找功能的定位混乱，经排查这是copy函数重新进行了区域选择导致，通过先保存原始选区结果后再copy解决了这个问题。

### 2024.01.01
- **开放所有类别**：上周发布时只支持Arxiv上几个类别，然后陆续不少读者申请增加自己想看的类别，于是尝试开放了所有类别，并允许在首页选择显示自己需要的类别；
- **Feed订阅支持**：不少读者有RSS订阅习惯，所以建议增加RSS链接，目前已经补充上去，但用的不是RSS格式而是更标准的Atom格式（几乎所有订阅器都同时支持两种格式）；
- **Markdown解析**：Kimi生成的FAQ一定程度上是Markdown格式的，对它进行解析可以有更好阅读体验；
- **点击次数显示**：[PDF]和[Kimi]后面多了一个数字，分别代表着两个按钮的点击次数，一定程度上代表了这篇论文的受欢迎程度
- **其他细节优化**：如移动端效果优化，[Kimi]稳定性优化、出错时的交互优化等。

## 交流
QQ交流群：67729435，微信群请加机器人微信号spaces_ac_cn
