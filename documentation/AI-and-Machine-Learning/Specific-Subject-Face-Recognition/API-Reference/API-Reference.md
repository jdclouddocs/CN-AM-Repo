# 特定人物识别

## 一、接口描述 
### 1. 功能描述  
  特定人物识别主要用于对传入的图片中所有人脸进行分析，判断是否为特定审核人物。
### 2. 能力说明：  
  目前可支持国内外政要人物，也可以支持明星演员，运动员，名人等公众人物或进行自定义人物审核库，根据自己的业务进行配置人物的审核策略。
### 3. 接口数据要求：  
> 1. 图片格式：支持jpeg(jpg)及png图片
> 2. 图片像素：最小 48 \* 48 像素，最大 4096 \* 4096 像素
> 3. 图片大小：小于2MB

### 4. 接口使用：  
  平台为每个API提供试用体验服务，您在AI市场选择“免费试用”规格下单后，即可开始体验业内领先的人工智能API服务。
免费试用服务具有调用量、QPS限制，如需更高性能的API服务，可以提交咨询工单，联系京东AI扩容购买。

在获得使用权限后，您可使用已经封装好的SDK/参照[接口鉴权](https://aidoc.jd.com/user/auth.html)规则进行相应开发，整体流程详见   [接入流程](https://aidoc.jd.com/user/flow.html)  

## 二、请求说明
### 1. 接口地址 ：
```
http://192.168.0.162:8080/PoliticiansRecognition_chanchuangyun
```
### 2. 请求方式：  
https  `post`aiapi.jd.com/jdai/PoliticiansRecognition_chanchuangyun
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
Content-Type | String | 是 | application/octet-stream | 标准编码格式

#### （3）body请求参数
业务请求参数

名称 | 类型 | 必填 | 示例值 | 描述
------|-----|-----|-----|-----
无 | Binary | 是 | 略 | 图片文件的二进制流

### 4、请求代码示例
建议您使用我们提供的SDK进行调用，SDK获取及调用方式详见本页一接口描述中的4接口使用

## 三、返回说明
### 1、返回参数
#### （1）公共返回参数  

名称 | 类型 | 示例值 | 描述
------|-----|-----|-----
code | string | 1000 | 参见下方错误码-系统级错误码
charge | boolean | false 或 true | false：不扣费， true：扣费
remain | long | 1305 | 按天计算剩余调用次数
msg | string | 查询成功 | 参见下方错误码-系统级错误码
result | object | {...} | 查询结果

#### （2）业务返回参数

result参数信息

名称 | 类型 | 示例值 | 描述
------|-----|-----|-----
status|	int|	0|	参照四、错误码-业务错误码
message|	string|	"Success."|	参照四、错误码-业务错误信息
request_id| string| "hJe+Bn3QhgfE2BKQ/HsD5g=="| 请求id
name|	string|	"金正恩"|	检出的人物姓名，若为空值，则未检出

### 2、返回示例    

{"status":0,"message":"Success.","request_id":"hJe+Bn3QhgfE2BKQ/HsD5g==","name":"金正恩"}


