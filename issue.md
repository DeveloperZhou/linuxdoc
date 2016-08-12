[TOC]

1.第一坑: GITHUB换行符自动转换
> Git 由大名鼎鼎的 Linus 开发，最初只可运行于 *nix 系统，因此推荐只将 UNIX 风格的换行符保存入库。
> 安装好 GitHub 的 Windows 客户端之后，这个功能默认处于“自动模式”。当你在签出文件时，Git 试图将 UNIX 换行符（LF）替换为 Windows 的换行符（CRLF）；当你在提交文件时，它又试图将 CRLF 替换为 LF。
> **即为 *nix file(local)-->win file(trans)-->*nix file(remote)**
> 问题具体表现在，如果你手头的这个文件是一个包含中文字符的 UTF-8 文件，那么这个“换行符自动转换”功能 在提交时是不工作的(但签出时的转换处理没有问题)。猜测可能这个功能模块在处理中文字符 + CRLF 这对组合时直接崩溃返回了。

**解决**
**$ git config --global core.autocrlf false**














