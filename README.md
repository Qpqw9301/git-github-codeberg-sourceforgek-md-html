# git/codeberg/github/sourceforgek基础教程，md/html语法，静态/动态网页制作托管发布教程 
&ensp;&ensp;目的：可以用于免审核免代理的代码托管，网络文章发布，资料文件上传分享，制作发布个人网页和博客，请勿用于非法用途               
***
     目录
     一.git和开源代码托管平台发布管理 （小文件传输分享）      
     二.sourceforgek代码托管平台使用指南（无限容量支持大文件传输分享）     
     三.md/html文件语法和书写       
     四.静态网页制作和发布  
     五.动态网页制作和发布  


***
## 一.git/gitcode/github基础教程     
     
- 注册codeberg账户，       
登陆 创建新项目 ,仓库名和仓库说明随意，开源协议可以设置 gpl3 or later 

- 安装git工具                    
对于debian及其下游分支,打开终端模拟器，输入         
          sudo apt install git         
对于archlinux及其下游分支，输入             
          sudo pacman -S git   
对于fedora及其下游分支，输入           
         sudo dnf install git    
对于win和mac,请自行互联网检索安装教程                              
***                   
- 打开终端模拟器，从命令行创建一个新的仓库  （命令行上传同步多个文件比图形化网页内上传方便快速）                      
&ensp;&ensp;cd  目录               
进入某文件目录                      
&ensp;&ensp;mkdir xxx              
在该文件目录下创建名为xxx的新目录                   
&ensp;&ensp;cd 新目录                   
进入新目录                                  
  
- &ensp;&ensp;touch README.md               
目录下创建一个md说明文件，也可以用图形化文件管理器右键新建文件,可以用图形化文件管理或者命令行把要上传的文移入目录内                       
&ensp;&ensp;vim（或nano） README.md            
编辑md文件，可以用记事本或vscode等编辑，也可以图形化文件管理器进入编辑                       
- &ensp;&ensp;git init        
 初始化仓库            
- &ensp;&ensp;git config "用户名"                   
修改本地用户名 （可随意）           
&ensp;&ensp;git config  “邮箱地址”  
修改本地邮箱（可随意）                       
- &ensp;&ensp;git checkout -b main     
- &ensp;&ensp;git add README.md           
将README.md加入缓存区 (这里如果是添加或修改了多个文件可以 输入 git add .将所有修改过的文件加入缓存区 )              
- &ensp;&ensp;git commit -m "first commit"                   
 提交修改，添加提交信息       （这里输入git comir -m .可以提交多文件）                      
- &ensp;&ensp;git remote add origin https://codeberg.org/用户名/项目名.git           
 git链接到自己的项目仓库                    
- &ensp;&ensp;git push -u origin main                   
推送同步文件到gitcode,需要输入用户名和密码 ,从命令行推送已经创建的仓库                               
- 或者克隆别人的项目到本地修改后上传成自己的
- &ensp;&ensp;cd   目录
进入你要下载到本地的目录    
- &ensp;&ensp;git clone 项目地址            
然后本地编译修改，修改好以后       
- 修改本地文件的用户名和密码    
&ensp;&ensp;git config “用户名”  
修改用户名       
&ensp;&ensp;git config “邮箱地址”      
修改邮箱                

- 提交换成并保存和提交               
 &ensp;&ensp;git add .       
 &ensp;&ensp;git commit -m .       
 &ensp;&ensp;git remote add origin https://codeberg.org/用户名/项目名.git                 
 &ensp;&ensp;git链接到自己的项目仓库                  
&ensp;&ensp;git push -u origin main                   
#推送同步文件到gitcode,需要输入用户名和密码 ,从命令行推送已经创建的仓库

*** 
# 二. sourceforgek代码托管平台使用指南（无限容量支持大文件传输分享）  
教程请打开观看： https://sourceforge.net/projects/pureos-virtualbox/files/sourceforge.net/     
***

# 三.md/html文件语法规则    
Markdown语法和HTML语法   
https://markdown.com.cn/basic-syntax/       
##### md文件个人使用总结    
1. 一级标题前缀      &ensp;&ensp;&ensp;&ensp;                        #空格         
2. 二级标题 &ensp;&ensp;&ensp;&ensp; ##空格 三四级标题以此类推     
3. 换行  &ensp;&ensp;&ensp;&ensp;                段尾加两个空格        
3. 段首缩进半个字符&ensp;&ensp;&ensp;&ensp;                & ensp;（中间和后面无空格）          
缩进两个字符             & ensp;& ensp;& ensp;& ensp;    (&和ensp之间无空格)            
4. 重点文字加粗标记请在单词或短语的前后各添加两个星号或下划线比如   
** 内容 **（中间无空格）             
5. 链接语法          
[超链接显示名]-(超链接地址 "超链接标题")(中间无-)
6. 图片语法  ![ 图 片 alt ]-(图片链接 "图片标题") （中间无- ）     
链接在线图片  [![沙漠中的岩石图片](/assets/img/shiprock.jpg "Shiprock")](https://markdown.com.cn)      
7. 引用语法，要创建块引用，请在段落前添加一个 > 符号      
8. 列表语法 &ensp;&ensp;&ensp;&ensp;有序列表“1.空格“，&ensp;&ensp;&ensp;&ensp;无序列表 “-空格”     
例子
- 实例
1. 项目1
***   

9. 分隔线   ---或者***  (上下都需要加空白行)  ，例子如下        


 ---  
10. 添加目录段首加五个空格，比如
     
        ** 这是目录： **  
           一.          
           二.
           三.  

*** 

# 四.静态网页制作托管发布
#### 1.书写html网页文件，最简单的方法莫过于md转html,借助vscode的转换插件     
vscode官网 https://code.visualstudio.com/        
vscode的html转换插件 Markdown Preview Enhanced,打开vscode,点击扩展图标，搜索并下载安装此插件，然后将编译好的md文件用vscode打开，右键打开侧边栏预览，在预览框里右键选择export-html-保存为html文件即可生成静态网页。    
####  2.上传html网页并托管发布网页
 &ensp;&ensp;新建codeberg项目后，上传此html文件，自动生成网址，网址地址为 https://用户名.codeberg.page/项目名/网站名称                
&ensp;&ensp;可以导入别人的在线网页，方式为火狐浏览器打开网页-右键保存网页（完整保存）-修改保存文件名后，上传html文件和同名配置文件夹到gitcode生成新网址，网址为： https://用户名.codeberg.page/项目名/网站名称       
示例： https://E0D4B047x.codeberg.page/git-gitcode-make/静态网址示例.html          
&ensp;&ensp;跟换托管域名-略 

***       

# 五.制作动态网页并托管发布                
&ensp;&ensp;使用免费vps网址：https://dash.infinityfree.com/  
- 注册登陆后选择创建账户，申请域名，申请ssl加密证书（用于发布https加密），此过程需要数个小时，申请后等待后台完成，根据提升完成1-4的操作，然后即可在发布网页时选择安装             
- 打开控制面板，网页管理即可在线制作发布动态网页，这里可以选择在线模板，也可以导入 别人的在线网页，制作完并发布后，网页为http而非https,要开启https,需要ssl证书申请成功后，在网页制作发布页的设置里开启https然后再次发布 
示例：          
           


                            




