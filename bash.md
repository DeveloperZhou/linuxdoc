[TOC] 
 
###Basic knowledge

1.文件描述符(File Descriptor)  
0 stdin	| 1 stdout | 2 stderr	
'<' <==> '0<' ; '>' <==> '1>'  

tee: 不影响原本 I/O ，将 stdout 复制一份到档案去  
cmd << text: 从命令行读取输入，直到一个与text相同的行结束  
cmd <<< word: 把word(而不是文件word)和后面的换行作为输入提供给cmd   
cmd <> file: 以读写模式把文件file重定向到输入，文件file不会被破坏。仅当应用程序利用了这一特性时，它才有意义  
  
> cmd >&n		把输出送到文件描述符n  
> cmd m>&n		把输出到文件符m的信息重定向到文件描述符n  
> cmd >&-		关闭标准输出  
> cmd <&n		输入来自文件描述符n  
> cmd m<&n		m来自文件描述符n  
> cmd <&-		关闭标准输入  
    
> cmd 2>file		把文件描述符2重定向到file，即把错误输出存到file中  
> cmd > file 2>&1	把标准错误重定向到标准输出，再重定向到file   
> cmd &> file		功能与上一个相同(或 cmd >& file)


###Configuration file location and function 
 
 
 
 
 
 
 
###Commands in common use 
 
1.type ¶type [-tpa] name¶   
> 不加任何选项与参数时, type会显示出name是外部指令还是bash内建指令   
> -a: 会由PATH变数定义的路径中, 将所有含name的指令都列出来，包含alias 
 
 
###Useful methods  
 
1.变数内容的删除、取代与替换   
**${** variable#/\*local/bin: **}**    
上面的特殊字体部分是关键字！用在这种删除模式所必须存在的   
${ **variable** #/\*local/bin:}   
这就是原本的变数名称   
${variable **#** /\*local/bin:}   
这是重点！代表『从变数内容的最前面开始向右删除』，且仅删除最短的那个   
${variable# **/*local/bin:** }   
代表要被删除的部分，由于#代表由前面开始删除，所以这里便由开始的/写起   
 
『从前面开始删除变数内容』 
\#: 符合取代文字的『最短的』那一个;   
\#\#：符合取代文字的『最长的』那一个;   
 
『从后面向前删除变数内容』 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
###Shortcuts 
 
|ctrl+u/ctrl+k|分别是从游标处向前删除指令串及向后删除指令串|   
|ctrl+a/ctrl+e|分别是让游标移动到整个指令串的最前面或最后面|   
 
 
###Attention points 
 
 
 
 
 
 
