# accessibilitymanager_fixed 
 A fixed version of the “WuDi-ZhanShen/AccessibilityManager”.From：https://github.com/WuDi-ZhanShen/AccessibilityManager



## about this application

Thanks to the original author
<a href="https://github.com/WuDi-ZhanShen/">  
WuDi-ZhanShen
</a>

原地址链接：https://github.com/WuDi-ZhanShen/AccessibilityManager

无意间发现的一个可以替代xposed模块“无障碍deamon”的app，新版无障碍deamon1.0.4老是开启无障碍失败，降级到1.02版本之后貌似在新版的lsposed上不能很好的运行，时好时坏。

Inadvertently found an app that can replace the xposed module "无障碍deamon". The new version of it（1.0.4） always fails to enable Accessibility Settings. After being downgraded to version 1.02, it seems that it can't run well on the new version of lsposed.

accessibilitymanager可以自动开启无障碍而且可以在后台进行保活，比magisk上的模块好用。

It can automatically replace accessibility settings and keep alive in the background, which is better than the module on magisk in my device.

此安装包修复了在安卓9（miui11.0.2）上闪退的情况，因为原作者貌似好久没更新了，所以我自己去Android studio上deb了一下。发现是在创建无障碍列表时引发的崩溃，显示是有一个item是null。在查看了存储无障碍条目的xml后没发现异常，里面也没有空值，而且该问题是在我使用这个软件大概一个月后出现的。可能是某些软件的无障碍服务名字的问题。我为了修复这个问题，在创建列表时添加一个if else判断，对null值进行处理。

Mechanical translation:

This installation package fixes the flashback on Android 9(miui11.0.2), because the original author seems to have not updated it for a long time, so I went to Android studio to deb it. It was found that the crash was caused when the Accessibility Settings list was created. It showed that one item was null. After View the xml for storing Accessibility Settings lists data, no abnormality was found, and there was no null value in it. And the problem appeared after I used this application for about a month. It may be a problem with the Accessibility Settings name of some application. These names have special characters.In order to fix this problem, I added an if else judgment when application created the list to deal with null values.

![image](https://github.com/long778/accessibilitymanager_fixed/blob/main/IMG_20240919_014108.jpg)
