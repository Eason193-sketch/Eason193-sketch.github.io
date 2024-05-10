# PX4-Autopilot仿真构建

本教程是基于ubuntu20.04构建的，如果不是使用该版本的ubuntu请谨慎参考
如果你还没有开始任何配置，跳转链接： [Fast-250-drone](https://gitee.com/pn_code/Fast-Drone-250 "Fast-250-drone")，如果你是第一次配置，请阅读以下注意事项.

* 先git clone 该项目，后安装glog，ceres,这两个在项目的3rd.zip下
* ./autogen.sh && ./configure && make && sudo make install之前先添加可执行权限chmod +x *
* 对于realsense-viewer的配置，需要改变BIOS的secure boot，设置为disabled，具体善用搜索
* 文档中存在一个版本问题，需要将

```linux
sudo apt-get install liblapack-dev libsuitesparse-dev libcxsparse3.1.2 libgflags-dev libgoogle-glog-dev libgtest-dev
```

更改为

```linux
sudo apt-get install liblapack-dev libsuitesparse-dev libcxsparse3 libgflags-dev libgoogle-glog-dev libgtest-dev
```

* 对于realsense-viewer的配置，需要改变BIOS的secure boot，设置为disabled，具体善用搜索
* 对于plot-juggler的安装，请使用snap，具体善用搜索

## PX4-Autopilot的安装

* 请开启终端代理，不然会非常非常非常麻烦
* clash默认端口为7890，启动clash后在终端执行命令
  
```linux
set https_proxy=http://127.0.0.1:7890;set http_proxy=http://127.0.0.1:7890;set all_proxy=socks5://127.0.0.1:7890
```

* 参考官方文档解决一切问题： [PX4-Autopilot官方链接](https://docs.px4.io/main/en/dev_setup/dev_env_linux_ubuntu.html "PX4-Autopilot官方链接")
* 下载QGC
  
## ego-planner仿真的配置

* 请跳转大佬up主的视频： [ego-planner仿真](https://www.bilibili.com/video/BV1mM4y1m7Vs/?spm_id_from=333.788&vd_source=3003b3957d9f36fe37207e82b7d8fbdf "课程") 从百度网盘（qaq）下载文件
* 请复制我写的模型到合适的位置，注意由于版本问题，建议不要bash up主PX4-Autopilot中的文件，因为很可能之后就要重装了哈哈哈
* 自己在第六七讲的文件下grep -rn iris_D435i一下，将这个改成iris
* 之后就直接照着UP主的课程跑仿真吧，打工去吧年轻人（qaq）