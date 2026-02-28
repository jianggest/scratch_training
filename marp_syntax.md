# Marp 语法介绍

Marp（Markdown Presentation Ecosystem）是一种基于 Markdown 的幻灯片制作工具。使用简单的 Markdown 语法，可以快速创建演示文稿。

---

## 基本结构

- 每个幻灯片使用 `---` 分隔。
- 支持主题、分页和注释等。

---

## 主题设置

```markdown
---
theme: default
class: lead
paginate: true
---
```

- `theme`：选择主题（如 `default`、`gaia` 等）。
- `class`：添加自定义样式类。
- `paginate`：启用页码。

---

## 标题和文本

```markdown
# 一级标题
## 二级标题
普通文本段落。
```

---

## 字体大小

可以通过内联样式或自定义 CSS 来控制字体大小：

```markdown
<span style="font-size: 24px">这是较大的文本</span>
```

全局修改可在幻灯片开头添加 `<style>`：

```markdown
<style>
section { font-size: 20px; }
</style>
```

主题也允许使用 `class` 定义不同大小的文字，例如 `lead` 或 `small`。

---

## 段落间距

通过 `margin` 或 `line-height` 调整段落间距：

```markdown
<p style="margin: 1.5em 0;">自定义间距的段落。</p>
```

同样可以在 `<style>` 块中设置全局规则：

```markdown
<style>
p { margin-bottom: 1em; line-height: 1.6; }
</style>
```

这些技巧可以让幻灯片排版更加美观。

---

---

## 列表

```markdown
- 无序列表项
- 第二项

1. 有序列表第一项
2. 第二项
```

---

## 图片和链接

```markdown
![图片描述](路径或URL)
[链接文本](https://example.com)
```

---

## 代码块

```markdown
```python
print("Hello, Marp")
```
```

---

## 幻灯片背景

```markdown
---
backgroundColor: #ffcc00
backgroundImage: url('背景图片.png')
---
```

---

## 分栏布局

```markdown
<!-- .column: style="width: 50%" -->

内容在两栏中

<!-- .column: style="width: 50%" -->

第二栏内容
```

---

## 备注

可以使用 `<!-- comment -->` 添加备注。

---

## 导出

使用 CLI 命令：

```
marp slide.md --pdf
```

更多信息请参考 [Marp 官方文档](https://marp.app/)。
