# 菜品识别


## 一、接口描述 
### 1. 功能描述  
菜品识别（food classification）API为用户提供菜品识别功能，输入一张菜品图片，返回识别结果。

### 2. 能力说明：   
输入图像限定为菜品图像，不能提供其他类别图像的识别能力。

### 3. 接口数据要求：  
- 图片格式：base64编码
- 图片类型：JPEG,BMP,PNG,GIF
- 图片像素尺寸：最小 50\*50 像素，最大 2048\*2048 像素
- 图片文件大小：小于2M

### 4. 接口使用： 

公测期间用户可以免费（0元）进行测试，根据[购买流程](../Pricing/Purchase-Process.md)下单后，即可开始体验业内领先的人工智能API服务。公测期间服务具有调用量、QPS限制，如需更高性能的API服务，请联系客服扩容购买。

使用接口前，需要先完成API的下单购买，然后可使用已经封装好的SDK/参照[接口鉴权](../Operation-Guide/Authentication.md)规则进行相应开发，整体流程详见[调用方法](../Operation-Guide/call-methods.md)  。

## 二、请求说明
### 1. 接口地址 ：

```
https://aiapi.jdcloud.com/jdai/FoodApi
```

### 2. 请求方式：  
https `post` aiapi.jdcloud.com/jdai/FoodApi

### 3. 请求参数 
#### （1）header请求参数
业务请求参数
<table>
   <tr>
      <th>名称</th>
      <th>类型</th>
      <th>必填</th>
      <th>示例值</th>
      <th>描述</th>
   </tr>
   <tr>
      <td>Authorization</td>
      <td>string</td>
      <td>是</td>
      <td>JDCLOUD2-HMAC-SHA256Credential=access...</td>
      <td>签名</td>
   </tr>
</table>


#### （2）body请求参数
业务请求参数
<table>
   <tr>
      <th>名称</th>
      <th>类型</th>
      <th>必填</th>
      <th>示例值</th>
      <th>描述</th>
   </tr>
   <tr>
      <td>image</td>
      <td>string</td>
      <td>是</td>
      <td>{"image":"4AAQSk..."}</td>
      <td>图像base64编码</td>
   </tr>
</table>

### 4、请求代码示例
建议您使用我们提供的SDK进行调用，SDK获取及调用方式详见[sdk的使用方法](../Operation-Guide/Use-Sdk.md)



## 三、返回说明
### 1、返回参数
#### （1）公共返回参数

<table>
   <tr>
      <th>名称</th>
      <th>类型</th>
      <th>示例值</th>
      <th>描述</th>
   </tr>
   <tr>
      <td>code</td>
      <td>string</td>
      <td>10000</td>
      <td>参见下方错误码-系统级错误码</td>
   </tr>
      <tr>
      <td>charge</td>
      <td>boolean</td>
      <td>false 或 true</td>
      <td>false：不扣费， true：扣费</td>
   </tr>
      <tr>
      <td>remain</td>
      <td>long</td>
      <td>1305</td>
      <td>按天计算剩余调用次数</td>
   </tr>
      </tr>
      <tr>
      <td>msg</td>
      <td>string</td>
      <td>查询成功</td>
      <td>参见下方错误码-系统级错误码数</td>
   </tr>
      </tr>
      <tr>
      <td>result</td>
      <td>object</td>
      <td>{...}</td>
      <td>查询结果</td>
   </tr>
</table>

#### （2）业务返回参数

<table>
   <tr>
      <th>名称</th>
      <th>类型</th>
      <th>示例值</th>
      <th>描述</th>
   </tr>
   <tr>
      <td>status</td>
      <td>int</td>
      <td>1000</td>
      <td>参照四、错误码-业务错误码</td>
   </tr>
   <tr>
      <td>message</td>
      <td>string</td>
      <td>OK</td>
      <td>参照四、错误码-业务错误码</td>
   </tr>
   <tr>
      <td>result</td>
      <td>string</td>
      <td>红烧肉</td>
      <td>返回菜品识别结果</td>
   </tr>
   <tr>
      <td>used_time</td>
      <td>int</td>
      <td>606</td>
      <td>整个请求花费的时间，单位为毫秒</td>
   </tr>
</table>

### 2、返回示例  


```
{
    "code": "10000",
    "charge": false,
    "remain": 0,
    "msg": "查询成功",
    "result": {
   			"message":"ok ",
   			"status": 1000,
   			"used_time": 606 
   			"result": "红烧肉"
    }
}
```
