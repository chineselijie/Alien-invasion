# python项目－－外星人入侵

> 所用python版本:python3
> 所用系统为深度Linux系统

深度Linux系统根据Debian系统开发，是作为最早的Linux发行版之一。

**首先安装好python3版本**
## 安装python3
```bash
$ sudo apt-get install python3
```
## 测试是否安装成功
```bash
$ python3
# 如果出现python3的版本信息，则表示安装成功，出错则失败
```

**还需要提前安装好pygame，才能执行代码**
## 安装pygame
```bash
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


## 测试是否安装成功
```bash
$ python3
>>> import pygame
# 如果没有报错则表示成功，出错则表示失败
```

## 运行程序
```bash
$ python3 alien_invasion.py
# 然后就会出现游戏界面，如果出错，请检查pip或者pygame是否安装成功
```

## 个性化设置
> 在**settings.py**文件中，可以修改屏幕长和宽，还有背景颜色以及飞船子弹等设置

```python
class Settings():
    """存储外星人入侵游戏的所有设置的类"""

    def __init__(self):
        """初始化游戏的设置"""
        # 屏幕设置
        self.screen_width = 1000  # 设置屏幕宽度
        self.screen_height = 600  # 设置屏幕高度
        self.bg_color = (230,230,230)  # 设置颜色，可参考最下面注1.

        self.ship_speed_factor = 1.5 # 设置飞船的左右移动的速度，可根据个人改动
        
        self.bullet_speed_factor = 1  # 每次发射几颗子弹
        self.bullet_width = 3  # 设置子弹宽度
        self.bullet_height = 15  # 设置子弹高度
        self.bullet_color = 60,60,60   # 设置颜色，可参考最下面注1.
        self.bullets_allowed = 3 # 限制子弹数量，第一颗子弹到达屏幕顶端，第三颗刚好射出而计算
```







> 注1：在Pygame中，颜色是以RGB值指定的。这种颜色由红色、绿色和蓝色值组成，其中每个值的可能取值范围都为0~255。颜色值(255, 0, 0)表示红色，(0, 255, 0)表示绿色，而(0, 0, 255)表示蓝色。通过组合不同的RGB值，可创建1600万种颜色。在颜色值(230, 230, 230)中，红色、蓝色和绿色量相同，它将背景设置为一种浅灰色。