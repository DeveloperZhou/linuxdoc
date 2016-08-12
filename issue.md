[TOC]

1.第一坑: GITHUB换行符自动转换  

> Git 由大名鼎鼎的 Linus 开发，最初只可运行于 *nix 系统，因此推荐只将 UNIX 风格的换行符保存入库。  
> **即为 *nix file(local)-->win file(trans)-->*nix file(remote)**  

Update:  
最后发现原来是markdown本身有的语法导致的，解决方法是在最后加上两个空格或者使用两个换行符  ！

**解决**  
**$ git config --global core.autocrlf false**  












