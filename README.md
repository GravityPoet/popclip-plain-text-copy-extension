# Plain Text Copy PopClip Extension

一个静默复制纯文本的 PopClip 扩展。

## 功能

- 只向剪贴板写入 `public.utf8-plain-text`。
- 去除源应用附带的 HTML、RTF、字体、字号、颜色和链接样式。
- 不显示 PopClip 的“已复制”提示。
- 原样保留所选文字中的空格、换行和字符。
- 完全离线运行，不联网，也不上传选中文字。

## 安装

1. 前往 [Releases](https://github.com/GravityPoet/popclip-plain-text-copy-extension/releases/latest)。
2. 下载 `PlainTextCopy.popclipextz`。
3. 双击安装包，并在 PopClip 中允许安装。

## 使用

选中文字后，点击 PopClip 操作栏中的“纯文本复制”图标。之后可以在任意应用中使用 `Command+V` 粘贴。

## 实现

扩展使用 PopClip 官方 JavaScript API 的 `pasteboard.text` 属性写入剪贴板。官方文档明确说明，该属性对应纯文本类型 `public.utf8-plain-text`，并且不会显示“Copied”通知：

- [PopClip JavaScript API：Pasteboard](https://pilotmoon.github.io/popclip-types/interfaces/Pasteboard.html)

## 兼容性

- macOS
- PopClip build 4586 或更高版本

## 源码

扩展源码位于 [`PlainTextCopy.popclipext`](./PlainTextCopy.popclipext)。
