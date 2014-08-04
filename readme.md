
Build:

```
# install gulp globally, npm install
gulp build
gulp deploy # put generated dist into this repo gh-pages branch
```

Summary:

```
1 到店里，发现要排队，入口：
  商家的二维码（url: appUrl/<shopid>）
  百度轻应用（appUrl， location， 再选到商家）

2 进入排队界面，开始排队
线上流程：（提交信息（选人数），约号码，其他信息（））
线下流程：
Tip: 线上/线下的号要统一。

3 进入排队/拼座流程主页面
（一般流程：进入求拼，然后进入可拼招人聊天拼桌）
求拼：顾客点击求拼，显示为4缺1，或6缺2。点击确认后进入『可拼列表』

可拼列表：列表中显示：4缺1，前面有3位号。
                                         6缺2，前面有2位号。
                                           ……
可点击列表中某一选项，进入聊天界面，开始商讨拼桌事宜。如果『拼桌发起者』同意，则，两号合并为发起者的号。
（限定条件：求拼人数小于选拼桌的可拼人数）

Event: 服务员通过管理界面（如三列： 四人桌，六人，八人），有一个空下的四人桌，四人桌面的第一位的号（这里很容易加一个推送通知的功能）

原则：边角料（选最接近（而且大于）人数的桌型）
```


API:

```
商家列表：
定位到商家：

商家现状（多少人排队）- ws
提交信息（多少人吃，约号，需检查位置） - 基于 deviceId 等

提交求拼：
商家可拼详情：（客户端来 filter） - ws

进入聊天： 基于 deviceId - ws - 

同意后并单：

已入座：
```

Prenstation:

```
ls -al materials/images |awk '{print "!["$9"](./materials/images/"$9")"}'
```

![onefan.001.jpg](./materials/images/onefan.001.jpg)
![onefan.002.jpg](./materials/images/onefan.002.jpg)
![onefan.003.jpg](./materials/images/onefan.003.jpg)
![onefan.004.jpg](./materials/images/onefan.004.jpg)
![onefan.005.jpg](./materials/images/onefan.005.jpg)
![onefan.006.jpg](./materials/images/onefan.006.jpg)
![onefan.007.jpg](./materials/images/onefan.007.jpg)
![onefan.008.jpg](./materials/images/onefan.008.jpg)
![onefan.009.jpg](./materials/images/onefan.009.jpg)
![onefan.010.jpg](./materials/images/onefan.010.jpg)
![onefan.011.jpg](./materials/images/onefan.011.jpg)
![onefan.012.jpg](./materials/images/onefan.012.jpg)
