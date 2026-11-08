+++
author = "Hugo Authors"
title = "Emoji 支持"
date = "2023-11-01"
description = "在Hugo中使用Emoji的指引"
tags = [
    "emoji",
]
+++

可以在一个 Hugo 项目中通过多种方式启用 Emoji。
<!--more-->
[`emojify`](https://gohugo.io/functions/emojify/) 函数可以被直接在模板或 [Inline Shortcodes](https://gohugo.io/templates/shortcode-templates/#inline-shortcodes) 中调用。

若要全局启用 emoji，在你的网站的 [配置](https://gohugo.io/getting-started/configuration/) 中将 `enableEmoji` 设置为 `true`，然后你就可以直接在内容文件中输入 emoji 的简写代码；例如：

<p><span class="nowrap"><span class="emojify">🙈</span> <code>:see_no_evil:</code></span>  <span class="nowrap"><span class="emojify">🙉</span> <code>:hear_no_evil:</code></span>  <span class="nowrap"><span class="emojify">🙊</span> <code>:speak_no_evil:</code></span></p>
<br>

[Emoji 速查表](http://www.emoji-cheat-sheet.com/) 是 emoji 简写代码的有用参考。

***

**注** 上述步骤可以在 Hugo 中启用 Unicode 标准的 emoji 字符和序列，但是这些字形的呈现取决于浏览器和平台。要给 emoji 设置样式，你可以使用第三方 emoji 字体或字体堆栈；例如：

{{< highlight html >}}
.emoji {
  font-family: Apple Color Emoji, Segoe UI Emoji, NotoColorEmoji, Segoe UI Symbol, Android Emoji, EmojiSymbols;
}
{{< /highlight >}}

{{< css.inline >}}
<style>
.emojify {
	font-family: Apple Color Emoji, Segoe UI Emoji, NotoColorEmoji, Segoe UI Symbol, Android Emoji, EmojiSymbols;
	font-size: 2rem;
	vertical-align: middle;
}
@media screen and (max-width:650px) {
  .nowrap {
    display: block;
    margin: 25px 0;
  }
}
</style>
{{< /css.inline >}}
