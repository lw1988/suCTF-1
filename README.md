# suCTF
网络攻防平台  
链接: https://pan.baidu.com/s/1dFo3wcD 密码: isxj  
做了简单的改版，但是，欢迎词需要改改~  
#系统要求  
 Ubuntu 16.04 32位  
#搭建步骤  
先解压网盘文件  
sudo apt install python-pip  
//将网盘文件拖入一个文件目录下(利用xftp)  
cd suCTF  
sudo pip  install --index https://pypi.mirrors.ustc.edu.cn/simple/ --upgrade pip  
sudo pip install gunicorn  
gunicorn --bind 0.0.0.0:8000 -w 4 "CTFd:create_app()"  

#如果想提示中文的欢迎语，请在\suCTF\CTFd中的views.py的顶部增加 # -*- coding: utf-8 -*-    
