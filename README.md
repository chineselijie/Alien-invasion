# python项目－－外星人入侵
"""
所用python版本:python3
"""

## 武装飞船
### 安装pygame
```python
# 首先查看是否安装pip
$ pip --version # 如果没有输出相关版本信息就需要安装
$ wget https://bootstrap.pypa.io/get-pip.py # 下载pip
$ sudo python3 get-pip.py # 安装pip
$ pip --version # 查看pip版本信息

$ sudo apt-get install python3-dev mercurial
$ sudo apt-get install libsdl-image1.2-dev libsdl2-dev libsdl-ttf2.0-dev # 安装pygame依赖库
$ sudo apt-get install libsdl-mixer1.2-dev libportmidi-dev
$ sudo apt-get install libswscale-dev libsmpeg-dev libavformat-dev libavcodec-dev
$ sudo apt-get install python-numpy #　启用pygame高级功能,添加额外的库文件
# 安装pygame
$ hg clone https://bitbucket.org/pygame/pygame
$ cd pygame && python3 setup.py build
$ sudo python3 setup.py install
```

```python
# 测试是否安装成功
$ python3
>>> import pygame
# 如果没有报错则表示成功，出错则表示失败
```

### 开始游戏项目

https://ehmatthes.github.io/pcc/solutions/README.html