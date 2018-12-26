# virtualenv
#python
安装
sudo pip3 install virtualenv
```
virtualenv venv  //创建一个名为venv的虚拟环境
virtualenv -p /usr/bin/python3.5 env

source venv/bin/activate  //进入venv的虚拟环境

查看虚拟环境中的pip安装包
pip list

开发完成把环境中安装包依赖名称导出
pip freeze > requirements.txt

退出虚拟环境
deactivate

删除虚拟环境

rm -rf venv

```