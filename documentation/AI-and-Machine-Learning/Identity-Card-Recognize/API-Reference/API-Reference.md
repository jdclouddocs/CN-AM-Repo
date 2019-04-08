# 身份证识别

## 一、接口描述 

### 1. 功能描述  

  识别二代居民身份证正反面的关键字段识别，包括姓名、性别、民族、出生日期、住址、身份证号、签发机关、有效期限，识别准确率业内领先，稳定可靠
  
### 2. 接口数据要求：  
> 1. 图片格式：jpg、jpeg、png、jfif
> 2. 图片大小：小于1M 

### 4. 接口使用：  
  平台为每个API提供试用体验服务，您在AI市场选择“免费试用”规格下单后，即可开始体验业内领先的人工智能API服务。
免费试用服务具有调用量、QPS限制，如需更高性能的API服务，可以提交咨询工单，联系京东AI扩容购买。

在获得使用权限后，您可使用已经封装好的SDK/参照[接口鉴权](https://aidoc.jd.com/user/auth.html)规则进行相应开发，整体流程详见   [接入流程](https://aidoc.jd.com/user/flow.html)  

## 二、请求说明
### 1. 接口地址 ：

```
https://aiapi.jd.com/jdai/ocr_idcard_chanchuangyun
```
### 2. 请求方式：  
https  `post`aiapi.jd.com/jdai/ocr_idcard_chanchuangyun
### 3. 请求参数    
#### （1）query请求参数  
公共请求参数  

名称 | 类型 | 必填 | 示例值	| 描述
------|------|-----|-----|-----
appkey | String | 是 | 80d2b762ecb86593f9668526920f46c	 | 您的appkey，可在买家中心控制台中获取  
timestamp | long | 是 | 1541491668060 | 请求的时间戳，精确到毫秒，timestamp有效期5分钟  
sign | String | 是 | 2e148773a0337a8f2200ba90d445f083	 | 签名，根据规则MD5(sectetkey,timestamp)， 

#### （2）header请求参数
业务请求参数

名称 | 类型 | 必填 | 示例值 | 描述
------|-----|-----|-----|-----
Content-Type | String | 是 | image/jpg | 标准编码格式

#### （3）body请求参数
业务请求参数

名称 | 类型 | 必填 | 示例值 | 描述
------|-----|-----|-----|-----
无 | binary | 是 | 无 | 图片内容，传入图片

### 4、请求代码示例
建议您使用我们提供的SDK进行调用，SDK获取及调用方式详见本页一接口描述中的4接口使用

## 三、返回说明
### 1、返回参数
#### （1）公共返回参数  

名称 | 类型 | 示例值 | 描述
------|-----|-----|-----
code | string | 1001 | 参见下方错误码-系统级错误码
charge | boolean | false 或 true | false：不扣费， true：扣费
remain | long | 1305 | 按天计算剩余调用次数
msg | string | 查询成功 | 参见下方错误码-系统级错误码
result | object | {...} | 查询结果

#### （2）业务返回参数
result参数信息

名称 | 类型 | 示例值 | 描述
------|-----|-----|-----
code|	int|	0|	参照四、错误码-业务错误码
message|	string|	success|	状态码描述
request_id|	string|	cb4f53b8c60e9589445cc4cd895cf5b6|	为方便定位问题的32位uuid
resultData|	object|	{...}|	返回识别结果

resultData参数信息

名称 | 类型 | 示例值 | 描述
------|-----|-----|-----
birthday | String | 1996-06-22 | 出生日期
address | String | 江苏省南通市开发区星海花园44幢505室 | 住址
gender | String | 女 | 性别
nationlity | String | 汉 | 名族
issuing_authority | String | 苏州市公安局姑苏分局 | 签发机关
valid_to | String | 2035-12-03 | 终止有效日期
valid_from | String | 2015-12-03 | 起始有效日期   
name | String | 葛钰瑶 |  	姓名  
id | String | 32062319960622626X | 公民身份号码  

### 2、返回示例   


```
{
    "code":1000,
    "charge":false,
    "remain":0，
    "msg":"查询成功"，
    "result":{
        "resultData": {
            "birthday": "1984年10月19日",
            "address": "成都市金牛区营通街6号1栋2单元1号",
            "gender": "女",
            "nationality": "汉",
            "issuing_authority": "",
            "valid_to": "",
            "name": "周静林",
            "valid_from": "",
            "id": "51010519841019026X"
        },
        "message": "success",
        "request_id": "329186449b547e2e19096b3dede18f55"，
        "code": 0
    }
}

```

