# 1：使用autodl作为解释器

设置——项目：你的项目——Python解释器——添加解释器——SSH
![alt text](./Pycharm连接autodl图片集/image.png)

填写autodl中的用户名、主机、端口、密码
![alt text](./Pycharm连接autodl图片集/image-1.png)

选择系统解释器/System Interpreter  
解释器/Interpreter：远程服务器的python解释器地址/相当于本地conda环境中的一格  
同步文件/Sync folders：本地现在的项目地址 与  远程服务器中哪个目录关联同步
![alt text](./Pycharm连接autodl图片集/image-2.png)

这时候已经训练模型的时候使用的是autodl中的A100了

注意！！！
因为使用的是远程服务器了，所以路径也切换成远程服务器了，不能使用本地数据集的路径！！！
![alt text](./Pycharm连接autodl图片集/image-3.png)


# 2：实现本地项目目录与远程项目目录映射绑定

工具——部署——配置——连接
![alt text](./Pycharm连接autodl图片集/image-4.png)
![alt text](./Pycharm连接autodl图片集/image-5.png)
根路径选择哪个在远程主机中就显示哪个目录
![alt text](./Pycharm连接autodl图片集/image-6.png)
![alt text](./Pycharm连接autodl图片集/image-7.png)
工具——部署——配置——映射
![alt text](./Pycharm连接autodl图片集/image-8.png)


# 3：在相互绑定以后本地代码更改远程也改的实时同步
同居——部署——选项
![alt text](./Pycharm连接autodl图片集/image-10.png)
设置——工具——SSH配置
![alt text](./Pycharm连接autodl图片集/image-9.png)

# 4：验证
本地添加一个test.py以后
远程也添加了test.py
![alt text](./Pycharm连接autodl图片集/image-11.png)
得益于：![alt text](./Pycharm连接autodl图片集/image-12.png)

