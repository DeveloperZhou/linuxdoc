[TOC]


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



###Shortcuts

|ctrl+u/ctrl+k|分别是从游标处向前删除指令串及向后删除指令串|  
|ctrl+a/ctrl+e|分别是让游标移动到整个指令串的最前面或最后面|  


###Attention points






