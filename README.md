# guards
主机入侵检测系统(HIDS)

### 项目进度
1. 2018/2/7 :完成文件监控方面（暂时只是单线程监控文件夹及其子文件中的文件）
2. 2018/2/8 :完成多进程监控主机文件夹及其子文件夹中的文件，采用一个进程监控一个文件夹的方式。<br/>
   2018/2/8 :初步增加配置文件功能，采用yaml格式作为配置文件<br>
   2018/2/8 :加入watchdog模块监控目标目录下的文件变化
3. 2018/2/9 :初步完成一个进程监控的demo，尚未写入配置文件，也没有为其分配进程
4. 2018/2/10:完成进程监控，实现主机进程状态检测，可及时发现新创建或者已关闭进程，<br>
             添加提权进程识别功能(暂不完善)
5. 2018/2/14:加入webshell静态检测数据库，通过使用python ssdeep库通过文件相似度对webshell进行静态检测
6. 2018/2/23:增加日志模块<br>
   2018/2/23:修正一些错误
---
### 系统所需软件
1. python-devel开发包
```shell
#ubuntu环境
sudo apt-get install python3.5-dev

#centos环境
yum install -y python3.5-devel
```
2. ssdeep安装方法
```shell
https://python-ssdeep.readthedocs.io/en/latest/installation.html
```