---
layout: post
title: android 屏幕适配, px和dp, sp换算公式
date: 2016-01-31
categories: blog
tags: [github,博客,jekyll]
description: 用Github + Jekyll搭建个人博客
---

##Andoird: 屏幕适配, px和dp, sp换算公式

### 换算公式:
* PPI =（长度像素数² + 宽度像素数²） / 屏幕对角线英寸数
* px = dp*ppi / 160
* dp = px / (ppi / 160)
* sp = px / (ppi / 160)

需要熟悉px,dp和sp这些换算公式以及做屏幕适配,我们要需要清楚以下几个概念:

> px: 是英文单词pixel的缩写，意为像素，屏幕上的点。我们通常所说的分辨率如480X800就是指的像素。在设计领域中，像素是用来计算数码影像的最小单位。计算机中显示的图像并非连续的线条组成，而是由许多肉眼看不见的小点组成。如果把影像放大数倍，会发现这些连续色调其实是由许多色彩相近的小点所组成，这些小点就是构成影像的最小单位“像素”。由于是最小的独立显示单位，px均为整数，不会出现0.5px的情况。

> dpi:  是Dots Per Inch的缩写,每英寸点数，即每英寸包含像素个数。比如320X480分辨率的手机，宽2英寸，高3英寸,每英寸包含的像素点的数量为320/2=160dpi（横向）或480/3=160dpi（纵向），160就是这部手机的dpi，横向和纵向的这个值都是相同的，原因是大部分手机屏幕使用正方形的像素点。


> dp: 也即dip，设备独立像素(虚拟像素)，device independent pixels的缩写，在不同的像素密度的设备上会自动适配,是Android特有的单位,比如:
     在320x480分辨率，像素密度为160,1dp=1px
        在480x800分辨率，像素密度为240,1dp=1.5px
        计算公式:1dp*像素密度/160 = 实际像素数 

> sp: 和dp很类似，一般用来设置字体大小，和dp的区别是它可以根据用户的字体大小偏好来缩放。

> PPI(density):是Pixels per inch缩写，每英寸上的像素数,即 "像素密度",density和dpi的关系为 density = dpi/160


### drawable- hdpi、drawable- mdpi、drawable-ldpi的区别：

(1) drawable-hdpi里面存放高分辨率的图片,如WVGA (480x800),FWVGA (480x854)

(2)drawable-mdpi里面存放中等分辨率的图片,如HVGA (320x480)

(3)drawable-ldpi里面存放低分辨率的图片,如QVGA (240x320)

### Android系统有自动渲染机制,会根据机器的分辨率来分别到这几个文件夹里面去找对应的图片。


xxhdpi | size=144*144   | dpi=480   | density=3|
--------------------|------------------|-----------------------|-----------------------|
xxhdpi | size=96*96   | dpi=320   | density=2|
hdpi|     size=72*72  |      dpi=240|   density=1.5|
mdpi|    size=48*48    |    dpi=160|   density=1|
ldpi|      size=36*36   |     dpi=120|   density=0.75|