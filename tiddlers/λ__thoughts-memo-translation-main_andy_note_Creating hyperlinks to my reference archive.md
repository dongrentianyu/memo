# 创建超链接到我的参考档案

原文：[Creating hyperlinks to my reference archive (andymatuschak.org)](https://notes.andymatuschak.org/z7xyZLXF3my9t5sPb7Kzdsg4pauz5mtbZqHWa)

在我的参考档案中，应该很容易建立持久的、可供人类阅读的资源链接。

例如，当提到一篇论文时，最好能链接到 PDF——可能是链接到一个特定的页面。我可以使用一个 `file://` 的 URL，但这带来了几个问题：

- 文件储存位置可能会变化

- 我无法链接到一个特定的页码

- URL 可能不具有可读性

- 这在 iOS 上肯定无法运行

如果能链接到一个自定义的协议（如 `ammref://`），那就更好了，它可以

- 重定向引用到具体文件

  - 如果需要的话，可以直接运行具体文件

- 避免将我捆绑在任何文件系统结构或阅读器应用程序上

- 支持可读的 URLs；例如

  - `ammref://Hattie/1994/VisibleLearning#p57`

这是很可行的。这将意味着：

- 制作一个简单的脚本，搜索有关联的参考资料

- 制作一个给出一个参考的 URL 的脚本

- 使得 Alfred 的工作流能够运行后者

------

## 参考文献

[Custom Skim URLs](http://www.dansheffler.com/blog/2014-07-02-custom-skim-urls/)

> 我希望能够在我的 Markdown 笔记中链接到 PDF 的任何一页，我知道我可以通过在浏览器中的 file://URL 的末尾添加 #35 来做到这一点，例如。但是我使用 [Skim](http://skim-app.sourceforge.net/)，在浏览器中阅读 PDF 是不可取的。此外，URL 最终会变得超长，而且有一些丑陋的转义符，如 %20 代表空格，这似乎没有必要，因为我所有的 PDF 都是用 [BibDesk](http://bibdesk.sourceforge.net/) 精心组织的。所以我设置了一个小的 AppleScript，它将解析一个以 sk:// 开始的自定义 URL，以获取 BibDesk 的引用键和页面索引，然后找出我想从 BibDesk 获取的 PDF，并在 Skim 中打开该 PDF，以获取正确的页面索引。

URN 在设计这个系统时可能也会有用：[Uniform Resource Name - Wikipedia](https://en.wikipedia.org/wiki/Uniform_Resource_Name)