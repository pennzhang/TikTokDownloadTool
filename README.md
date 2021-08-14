# 版权说明
本项目fork自[creatorMao TikTokDownloadTool](https://github.com/creatorMao/TikTokDownloadTool)。目的是为了增加个性化的功能，若想体验更多完善的功能请支持原作者的项目。

# 环境要求
- 请检查宿主机，是否安装了python3环境，并且配置了环境变量

- 请下载以下python库
~~~
    pip install requests
    pip install retrying
~~~
```
姜胡说
https://v.douyin.com/eofMRCa/
```
# 功能
- [x] 全量下载：下载指定博主主页下所有的无水印视频和图片
- [x] 增量下载：下载之前下载过全量的博主新更新的内容

1. 建议先使用全量下载功能，先下载一遍全部视频。
2. 再使用增量下载功能，定期下载即可。（全量下载以后，会将当前博主放到增量下载列表里，选择增量下载功能时，无需再复制链接）

# 使用方法
目前只支持源码运行，等功能完善后，再封装docker

## 1. Docker 
敬请期待

## 2. 命令行程序

请下载源码，在终端运行以下命令，进入程序。

~~~
python TikTokMulti.py
~~~
![python环境](./Resource/guide.jpg)

### 2.1 若输入1，选择全量下载。则需要复制抖音博主主页地址

<div style='display:flex;'>
    <img width='375px' height='667px' src='./Resource/userHomeStep1.jpg'>
    &nbsp;&nbsp;&nbsp;
    <img width='375px' height='667px' src='./Resource/userHomeStep2.png'>
    &nbsp;&nbsp;&nbsp;
    <img width='375px' height='667px' src='./Resource/userHomeStep3.png'>
</div>


#### 2.1.1 复制地址，进行下载。
ps:若遇到报错，请重新下载。基本上是服务器抽风

![step3](./Resource/fullDownload.jpg)


### 2.2 若输入2，进行增量下载。

![增量下载](./Resource/updateDownload.jpg)


## 3. 定时增量下载
Linux下，定时运行以下命令，可实现定时增量下载。从此解放双手~

~~~
# 此命令执行后，无需选择功能，直接进入增量下载模式
python3 autoDownload.py
~~~



# 说明

- 文件保存在Download文件里，以名称分类
![python环境](./Resource/download.jpg)

- 已下载视频通过sqlite3数据表记录