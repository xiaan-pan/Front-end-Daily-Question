# DOCTYPE 的作用是什么？

DOCTYPE 是 Document Type 的缩写，即文档类型。在 HTML 文档的开头，DOCTYPE 用来指定浏览器该如何解析 HTML 文档。它并不是 HTML 标签，而是一个引入文档类型定义（DTD）的声明。

HTML有很多版本，每个版本都对应着一种 DTD，常见的有以下几种：

- HTML 5：`<!DOCTYPE html>`
- HTML 4.01 strict：`<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN" "http://www.w3.org/TR/html4/strict.dtd">`
- HTML 4.01 transitional：`<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN" "http://www.w3.org/TR/html4/loose.dtd">`
- XHTML 1.0 strict：`<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">

DOCTYPE 的作用主要有两个方面：

1. 提供给浏览器正确的文档类型以决定使用哪种解析方式，从而确保 HTML 文档能够正确地被渲染；
2. 帮助浏览器解析 CSS，因为不同的 DTD 会影响 CSS 的解释和运行。

没有指定正确的 DOCTYPE 可能导致页面的兼容性问题，并可能导致浏览器不正确地解释文档内容。因此，为了保证网页的正确性和一致性，DOCTYPE 声明是必需的。