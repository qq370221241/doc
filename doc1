欢迎使用ShowDoc！
    
**简要描述：** 

1、接口传输的所有参数使用 UTF8 编码格式，包括签名。接口以 http/https的POST方式进行调用，以防数据被截取。
2、图片格式为jpg,png格式。大小为每个图片不超过1M，可参考DEMO的请求方式。


**请求URL：** 
- 测试环境：` http://10.8.18.202:7886/api/share-merchant/apply`
  
**请求方式：**
- POST 

**参数：** 

|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
|agentId |是  |string |代理商编号，由乐刷分配的接入方唯一标识，明文传输。测试环境固定为10。   |
|version |是  |string | 目前固定值1.0    |
|reqSerialNo     |否  |string | 请求流水号(全局唯一，建议为 yyyymmddXXXXXXXX，其中 XXXXXXXX 为 8 位顺序,目前只作为定位请求用)    |
|sign     |是  |string | 签名串，业务数据明文参与签名后经 Base64 编码的字符串。    |
|data     |是  |string | 业务数据明文字符串（Json格式，参照各个接口中输入参数说明）。    |



**data参数：** 

|参数名|必选|类型|说明|
|:---- |:---|:----- |-----   |
|merchantId |是  |string |商户号   |
|transactionId |是  |string |流水号,注意：交易成功请求分账时给交易成功的交易流水号；退货时请给相应的退货交易流水号  |
|orderId |是  |string |订单号   |
|commissionMerchantId|是|string|承担手续费商户号|
|shareDetail|是|json数组|分账的详细内容|


**shareDetail：** 

|参数名|必选|类型|说明|
|:---- |:---|:----- |-----   |
|merchantId |是  |string |商户号   |
|amount |是  |long |金额，单位：分   |
|remark |否  |string |备注   |


 **返回示例**

``` 
  {
"respCode":"000000",
"respMsg":"处理成功"
"reqSerialNo":"2017062300000001",
"version":"1.0",
"data":"{
		结算组返回内容
	}"
}
```

 **返回固定参数说明** 
 
|参数名|类型|说明|
|:-----  |:-----|-----                           |

 **备注** 

- 更多返回错误代码请看首页的错误代码描述


