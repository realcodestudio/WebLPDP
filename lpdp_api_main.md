# 叶桃防灾(LPDP)  开源APIs 官方文档


## <font color="\#3CB371">LPDP APIs 介绍</font>
- 欢迎来到叶桃防灾(LPDP)的API官方文档页。在这里，我们为开发者们整合准备了多个API以用于获取防灾相关数据或测试连接性能。<br>
- 叶桃防灾将不对这些API作限速限量处理，并始终保持免费， **<font color="#3CB371">直到我们无法运营服务器</font>** 。<br>

- Tips: 为了其他开发者着想，请您 **<font color="#FFAE32">不要 滥用/随意传播/过高速率访问</font>** 。若这些API对您或您的作品有帮助，您可以为我们 **[赞助一点小资金](/donate_us)** 来帮助我们更好的运营与不断改进~<br>


- 请注意：以下API均非官方数据源或爱好者数据源， **<font color="#FFAE32">并不能替代官方数据，最终数据请以官方发表内容和数据为准</font>** 。针对使用这些API接口产生的损失或伤亡，叶桃防灾不承担任何责任，若您选择使用叶桃防灾API则代表您同意我们的规定。详情内容请见 **[《叶桃防灾权利声明与免责声明》](/lpdp_statement)** <br>


- **<font color="#F0869B">叶桃防灾官网还在施工中...</font>**  可能会出现显示不正确的情况，敬请谅解。
- 此外，我们后续可能更换为 **<font color="#0E9FFF">Websocket连接</font>** 以传输这些数据替代现有的 **<font color="#9C3AFF">json文件读取</font>** 。

------



## 爱好者地震监测站点相关(施工中...)

### <font color="\#3CB371">AM.RD3C0 内蒙古鄂尔多斯市测站数据API</font>

- >**<font color="#3CB371">API描述:安装在内蒙古鄂尔多斯市的爱好者地震测站(Raspberry Shake 4D设备)观测到的数据 </font>** </font>

- **<font color="#FFAE32">注意：</font>** 该测站提供的数据已经过RS官方(Raspberry Shake)校准，但该数据不能替代官方测站数据使用，并且在测站附近地震时，该测站受到震动影响可能导致数据回传延迟或不稳定。

- **<font color="#0E9FFF">测站详细信息:</font>** 

  > [AM.RD3C0测站信息](/info_rd3c0)

- **<font color="#0E9FFF">API地址:(目前正在施工中...暂停访问。)**

  > ~~https://api.leafpeach.cn/lpeo/RD3C0.json~~
  
- **<font color="#0E9FFF">API内容说明:</font>**</font>
| 字段             | 数据类型 | 描述                                   | 例值                    | 提供条件 |
| ---------------- | -------- | -------------------------------------- | ----------------------- | -------- |
| name             | 字符串   | 观测点名称(叶桃防灾内命名)             | [叶桃]内蒙古 鄂尔多斯 1 | 始终提供 |
| <font color="#323232">name_n</font>           | <font color="#323232">字符串</font>   | <font color="#323232">观测点统一命名(编号) </font>                   | <font color="#323232"> AM.RD3C0 </font>                | <font color="#323232"> 始终提供 |</font>
| pga              | 数字     | 观测点PGA(地表峰值加速度 - 单位 cm/s²) | 0.17                    | 始终提供 |
| <font color="#323232">pgv </font>             | <font color="#323232">数字 </font>    | <font color="#323232">观测点PGV(地表峰值速度 - 单位 cm/s) </font>   | <font color="#323232">0.04 </font>                   | <font color="#323232">始终提供</font> |
| pgd              | 数字     | 观测点PGD(地表峰值位移 - 单位 cm)      | 0.002                   | 始终提供 |
| <font color="#323232">shindo_str </font>      | <font color="#323232">字符串 </font>  | <font color="#323232">观测点震度(字符串型) </font>                  | <font color="#323232">6+ </font>                     | <font color="#323232">始终提供 </font>|
| shindo           | 数字     | 观测点计测震度                         | -0.8                    | 始终提供 |
|<font color="#323232"> ce_intensity_str </font> | <font color="#323232">字符串 </font>  | <font color="#323232">观测点烈度(字符串格式化型) </font>            | <font color="#323232">9</font>                       | <font color="#323232">始终提供</font> |
| ce_intensiry     | 数字     | 观测点计测烈度                         | -1.1                    | 始终提供 |
| <font color="#323232">update_time </font>     | <font color="#323232">字符串 </font>  | <font color="#323232">数据更新时间(UTC+8) </font>                   | <font color="#323232">2023-07-14 17:16:15 </font>    | <font color="#323232">始终提供</font> |



## 图像数据相关

### **<font color="\#3CB371">Hi-Net 自动处理震源图 API</font>**

- >**<font color="#0E9FFF">API描述:每15分钟更新一次的日本地区的自动处理震源累计图像API</font>**</font> 

- **<font color="red">注意:</font>**</font> 该API提供的图像属NIED旗下的Hi-net自動処理震源マップ（Hi-Net自动处理震源图），非叶桃防灾团队产出，图像仅供参考，学习使用！该图像API上标识的内容均采用日本当地时间(JST; UTC+9)，在使用时请注意时间问题。**

- **<font color="#0E9FFF">API地址:</font>**</font>

  > 24小时 https://api.leafpeach.cn/image/hinet/hypo_24h.jpg
  >
  > 7日 https://api.leafpeach.cn/image/hinet/hypo_7d.jpg
  >
  > 30日 https://api.leafpeach.cn/image/hinet/hypo_30d.jpg

- **<font color="#0E9FFF">API内容说明:</font>**</font>

  | API参数  | 描述                                         | 提供条件 |
  | -------- | -------------------------------------------- | -------- |
  | hypo_24h | 至图像更新时，前24小时内所有的震源点累计图像 | 始终提供 |
  | <font color="#323232">hypo_7d</font>  | <font color="#323232">至图像更新时，前7天内所有的震源点累计图像</font>    | <font color="#323232">始终提供 </font>|
  | hypo_30d | 至图像更新时，前30天内所有的震源点累计图像   | 始终提供 |



## 文本数据服务相关


### **<font color="\#3CB371">叶桃防灾服务器时间同步API</font>**

- > **<font color="#0E9FFF">API描述:实时提供叶桃防灾数据处理服务器的时间数据来方便同步相关服务的时间</font>**</font> 

- **<font color="#0E9FFF"> API地址: </font>**

  > https://api.leafpeach.cn/sync_server_time.json
  
- **<font color="#0E9FFF"> API内容说明: </font>**
| 字段      | 数据类型 | 描述                           | 例值                | 提供条件 |
| --------- | -------- | ------------------------------ | ------------------- | -------- |
| time_gmt8 | 字符串   | 格式化后的时间数据(CST; UTC+8) | 2023-07-30 15:21:52 | 始终提供 |





------


API Docs Version 1.4

Update AT 2024/01/29 00:03(CST; UTC +8)
