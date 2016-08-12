
###VIM安装(debian)

1.Install vim var source code(git)  
//会自己生成一个vim文件夹
**$ git clone https://github.com/vim/vim.git
$ ./configure --with-features=huge --enable-pythoninterp --enable-rubyinterp --enable-luainterp --enable-perlinterp --with-python-config-dir=/usr/lib/python2.7/config/ --enable-cscope --prefix=/usr**    
![No Terminal Library Found when Compiling Vim](http://askubuntu.com/questions/158344/no-terminal-library-found-when-compiling-vim)  
[option]$ apt install ncurses-dev  
**$ make  
$ make install**  
  
2.Configure vim [.vimrc | .vimrc.bundle | .vim/]  







###VIM 常用命令  
  
1.每一行的行尾添加2个空格  
:%s/$/  /g  
  
  
  
  
  
  
  
  
####格式化    
