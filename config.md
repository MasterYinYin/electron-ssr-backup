# Electron-SSR在ubuntu18.04系统下的配置问题
## PAC模式可用但全局模式不可用

经检查，原因如下：

首先，PAC模式和全局模式有不同的配置端口，在软件中，配置/选项设置中可查看。

![image1](https://github.com/MasterYinYin/electron-ssr-backup/blob/gh-pages/Image/img1.png)

在切换为PAC模式时,在ubuntu/设置/网络中，网络代理模式会自动切换为自动，即
![image2](https://github.com/MasterYinYin/electron-ssr-backup/blob/gh-pages/Image/img2.png)

而当切换为全局模式时,在ubuntu/设置/网络中，网络代理模式会自动切换为手动，默认无代理端口，因此需要添加Http端口，如
![image3](https://github.com/MasterYinYin/electron-ssr-backup/blob/gh-pages/Image/img3.png)

此时即可使用全局模式。
