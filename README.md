# spider_zhihu_meizi
爬取知乎问题"平胸或者胸太大有给你带来什么困扰？"的图片和答案

## 文件说明
* images：存放妹子的图片
* data.txt：存放页面请求后获得数据
* src.ipynb 

## 环境配置
* 操作系统：Mac OS
* 开发语言：python 3.6
* IDE：jupyter notebook
* 浏览器：Chrome（版本75.0.3770.100）
* 需要用到的库：selenium、bs4、time、re、pandas、os

## 策略思路
知乎问题的主页为：https://www.zhihu.com/question/272446402

后面数字其实为问题ID，若想爬取其他问题的页面，修改后面的编码即可。

爬虫开始时，先用selenium模拟打开浏览器，现在selenium为3.x版本，需要下载相应的插件才能启动，否则会报错。

对于Chrome浏览器，插件下载地址：http://npm.taobao.org/mirrors/chromedriver/

对于火狐的话：https://github.com/mozilla/geckodriver/releases下载/

下载的时候必须选择与自己浏览器版本相照应的插件版本。

下载完成后解压，并把解压内容添加到python环境变量中去，又或者复制到浏览器安装目录文件中，又或者在代码允许selenium的时候制定插件路径（本次实验中使用的方法）。

代码运行后，会自动弹出新的浏览器，需要不停下拉到底部，才能加载到所有问题都显示在页面上，最后开始对页面进行解析。

