# accessibilitymanager_fixed

原地址链接：https://github.com/WuDi-ZhanShen/AccessibilityManager

无意间发现的一个可以替代xposed模块“无障碍deamon”的app，新版无障碍deamon1.0.4老是开启失败，降级到1.02版本之后貌似在新版的lsposed上不能很好的运行，时好时坏

accessibilitymanager可以自动开启无障碍而且可以在后台进行保活，比magisk上的模块好使。

此安装包修复了在安卓9（miui11.0.2）上闪退的情况，因为原作者貌似好久没更新了，所以自己去Android studio上deb了一下。发现是在创建无障碍列表时引发的崩溃，显示是有一个item是null，查看了读取的存储无障碍相关信息的xml后没发现异常，里面也没有空值，而且改问题是在我使用这个软件大概一个月后出现的。可能是某些软件的无障碍服务名字的问题，在创建列表时添加一个if else判断，对null值进行处理就好了。

![image](https://github.com/long778/accessibilitymanager_fixed/blob/main/IMG_20240919_014108.jpg)
