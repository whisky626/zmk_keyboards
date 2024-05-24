拿到之后首先清除蓝牙配对，方法：

1.按下mo4

![image](https://github.com/whisky626/zmk_keyboards/assets/129984996/0ca4ac33-1056-4bc6-abd8-b5320a9a51b8)


ly0
 * ------------------------------------------------------------------------------------------------------------------------
 * |       |   W   |   C   |   F   |   B   |-----------------------------------|      P   |   L   |   U   |   Y   |       | 
 * |   A   |   R   |   S   |   T   |   G   |-----------------------------------|      M   |   N   |   E   |   I   |   O   | 
 * |   J   |   Z   |   Q   |   D   |       | ----------------------------------|          |   H   |   V   |   K   |   X   | 
 * ------------------------|  MO 4 |  MO 2 | ----------------------------------|SPACE/LT 1|  LSHIFT |----------------------
 
2.切换第4层，再按下to 5，松手

ly4
 * --------------------------------------------------------------------------------------------------------------------------
 * |LS(TAB) |  LC(X)  |  LC(C) |  LC(V) |  LC(FSLH) |-----------------------------------|     |     |      |      | NUMLOCK | 
 * |  LC(A) |  LC(S)  |  LA(A) |  LC(F) |  LA(S)    |-----------------------------------|     |     |      |      |         | 
 * |  LC(Z) |  LC(Y)  |        |        |  LG(L)    | ----------------------------------|     |     |      |      |         | 
 * ----------------------------|        |           | ----------------------------------|     | to 5|------------------------
 
（注：此处绑定的to指令而非mo，意思是“到第5层”，所以按下to 5后可以松手。这主要是因为刷固件时重置完右手后无法维持mo按住的动作，左手会切回层4而不是维持在层5，这会导致找不到重置键）

3.此时整体切到第6层，按一下bt0表示切换到第一个蓝牙连接的设备，再按下bt_clr清除与该设备的连接。（注：键盘上清除后也要在对应电脑的蓝牙上手动忘记掉键盘设备）

 ly5
 * ---------------------------------------------------------------------------------------------------------------
 * |  BT0  |  BT1  |  BT2  |  BT3  |  BT4  |-----------------------------------|     |      |      |      |      | 
 * |       |       |       |       |       |-----------------------------------|     |      |      |      |      | 
 * |  boot | RESET | BT_CLR|       |  OUT  | ----------------------------------|     |      |      | RESET|  boot| 
 * ------------------------|       |       | ----------------------------------|     | TO 0 |---------------------
拿到之后需要这样操作：
bt0--bt_clr--bt1--bt_clr--bt2--bt_clr--bt3--bt_clr--bt4-- bt_cl--bt0
然后再在电脑蓝牙界面找到pippy_split选择配对，表示将电脑连接到bt0的位置。如果再与手机配对，按下bt1，再在手机蓝牙上选择配对，以此类推

4.按下to 0，回到默认层0


重置固件方法：
插上数据线（附赠的一分二数据线只有橙色口有数据传输功能，另一根仅供电），在第3步的基础上，先按右手boot键（切记），此时电脑文件资源管理器会弹出u盘NICENANO（E）,将right固件拉到该u盘；再按左手boot键，将left固件拉到u盘，完成，刷固件后会回到默认层第0层

其它解释：
Reset：重新运行当前的固件，正常情况下不会有什么影响
Out：切换usb与蓝牙的输出，如果既连接电脑数据线，同时蓝牙输出是bt1（手机）的情况下，此键用于切换

补充：
1.	上盖是磁吸的，拆的时候直接拔，卡得比较紧故上盖有两个磁铁位置没装，如果觉得翘边可以用附赠的磁铁用磁铁用胶水粘上去，没有就用502代替，注意磁铁接触面方向不要相斥
2.	如果刷固件操作顺序失误找不到boot键，拆开上盖，插上数据线用镊子或者导线短接主控从type-c口数第4个两侧焊孔2次，不分左右手顺序，再分别刷固件，最好是先刷左手固件再刷右手
3.	两侧type-c口的位置间隙有点大，为了美观可以用硅胶防尘塞塞住，可以等我选好型发链接，或者可以去定制金属铭牌
4.	键帽为了测试方便换成colmak配列，高度不一，觉得不美观辛苦手动换一下
