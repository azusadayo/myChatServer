# myChatServer
nginx mysql redis muduo库

原本的聊天服务器不能输入中文是mysql里设置的编码模式的问题，需要把db.cpp里的mysql_query(_conn, "set names gbk");改成mysql_query(_conn, "set names utf8mb4");


编译方式
cd build
rm -rf *
cmake ..
make

cd 到bin里分开执行Server和Client 需要在后面加上地址和端口号，client都连接nginx暴露的8000端口，Server的ip和端口需要在nginx的配置文件里做调整
