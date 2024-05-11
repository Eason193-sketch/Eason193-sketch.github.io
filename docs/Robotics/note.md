# 机器人导论复习

## 传感器

![img](https://yjapi.cmc.zju.edu.cn/sourceapi/uploads/2024/04/d86d6e67-f3e4-4808-a458-5af96af89bca.jpg) 

![img](https://yjapi.cmc.zju.edu.cn/sourceapi/uploads/2024/04/4aaf1357-55c1-4b58-b5d5-a78181f4534b.jpg) 

![img](https://yjapi.cmc.zju.edu.cn/sourceapi/uploads/2024/04/c6649ed3-f4c7-41c6-9c55-777150ab8f04.jpg)

![img](https://yjapi.cmc.zju.edu.cn/sourceapi/uploads/2024/04/f3ccb19e-c1f4-4702-aa8a-47ec8f409dae.jpg)

**tips**

* 手机的位置信号在室内由基站信号计算得到，

* 光电编码器测量轮子转了几圈，使用PWM波

* 减低PWM占空比和采样周期可以提高速度传感器精度

* 光纤陀螺仪，MEMS陀螺仪 

* 激光测距仪旋转测距，建图

* 双目测距范围为双相机距离的30倍左右

* 线性加速度计的功能



**搜索**

> 轮式机器人常用传感器
>
> > 



## 里程估计与定位

是相对定位问题

**里程**

* 电机码盘里程估计：正运动学问题
* 激光/视觉/IMU融合的历程估计

**概念**

* 定位：相对地图原点，误差有界，不实时提供

* 里程：从一个位置到另一个位置的变化估计，误差累积，实时提供

**定位**

* GPS：三点法估计，多路径问题选择最早回波
* 外部视觉系统
* 基于位置识别的定位(图像匹配)
* 里程估计，用定位修正



## 视觉

* 深度的获取: $ d=\frac{c}{2tan(\alpha/2)}$
* 被动光源受外部光源和尺寸的影响，难以测量深度信息

 