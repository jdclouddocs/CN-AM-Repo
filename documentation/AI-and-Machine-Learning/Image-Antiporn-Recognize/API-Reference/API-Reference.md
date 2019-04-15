# 智能鉴黄 #

## 一、接口描述 ##
  
### 1.功能描述 ###


基于业界领先的深度学习图像识别技术，对图片影像的肤色、姿态和场景等进行智能识别
，准确快速的输出每张图片“色情”、"低俗”、“性感”、“正常”的概率，其中色情图片准确
率高达 99.95%，有效的规避涉黄风险，让您的内容轻松过审核，成倍的解放审核人力！


### 2.接口数据要求 ###


(1)仅支持jpg,jpeg,png图片类型

(2)图片大小建议小于2M


### 3.接口使用 ###

公测期间用户可以免费（0元）进行测试，根据[购买流程](http://neuhub.jd.com/ai/api/image/pornIdentification)下单后，即可开始体验业内领先的人工智能API服务。公测期间服务具有调用量、QPS限制，如需更高性能的API服务，请联系客服扩容购买。


## 二、请求说明 ##

公共请求参数
<table>
   <tr>
      <th>名称</th>
      <th>类型</th>
      <th>必填</th>
      <th>示例值</th>
      <th>描述</th>
   </tr>
   <tr>
      <td>appkey</td>
      <td>string</td>
      <td>是</td>
      <td>80d2b762ecb86593f9668526920f46c</td>
      <td>您的appkey，可在买家中心控制台中获</td>
   </tr>
   <tr>
      <td>timestamp</td>
      <td>long</td>
      <td>是</td>
      <td>1541491668060</td>
      <td>请求的时间戳，精确到毫秒，timestamp有效期5分钟</td>
   </tr>
   <tr>
      <td>sign</td>
      <td>string</td>
      <td>是</td>
      <td>2e148773a0337a8f2200ba90d445f083</td>
      <td>签名，根据规则MD5(sectetkey,timestamp)</td>
   </tr>
</table>

### 1.GET请求方式 ###

query参数

名称 | 类型 | 必填 | 示例值	| 描述
------|------|-----|-----|-----
image_url | String | 是 | 略 | 图片完整url

header参数

名称 | 类型 | 必填 | 示例值	| 描述
------|------|-----|-----|-----
request url | String | 是 | http://aiapi.jd.com/jdai/cvImage_chanchuangyun | 请求地址
request method | String | 是 | GET | 请求方法


### 2.POST请求方式
header参数

名称 | 类型 | 必填 | 示例值	| 描述
------|------|-----|-----|-----
request url | String  | 是 | http://aiapi.jd.com/jdai/localCvImage_chanchuangyun | 请求地址
request method | String | 是 | POST | 请求方法
content type | String | 否 | application/octet-stream ,text/plain ... | 二进制流，文件类型..

body参数

名称 | 类型 | 必填 | 示例值	| 描述
------|------|-----|-----|-----
 无 | ByteArrayRequestEntity| 是 | 略 | 图片二进制流




### 3.请求代码实例 ###
建议您使用我们提供的SDK进行调用，SDK获取及调用方式详见本页一接口描述中的4接口使用

## 三、返回说明 ##
### 1.公共返回参数 ###
名称 | 类型 | 示例值 | 描述
------|-----|-----|-----
code | string | 1000 | 参见下方错误码-系统级错误码
charge | boolean | false 或 true | false：不扣费， true：扣费
remain | long | 1305 | 按天计算剩余调用次数
msg | string | 查询成功 | 参见下方错误码-系统级错误码
result | object | {...} | 查询结果

### 2.业务返回参数 ###

result参数信息

名称 | 类型 | 必填 | 示例值	| 描述
------|------|-----|-----|-----
status | int | 是 | 0	 | 状态码
message | String | 是 | 正常 |  具体消息
request_id | String | 是 | 03ac182a-03e1-4802-840b-a33bd985619d	 | 请求id
sexyScore | double | 是 | 0.2877 | 性感分数
pornScore | double | 是 | 0.2183 | 成人分数
vulgarScore | double | 是 | 0.1532 | 低俗分数
normalScore | double | 是 | 0.3409 | 正常分数

### 3.返回实例 ###
```
{
    "code":"10000",
    "charge":false,
    "remain":0,
    "msg":"查询成功",
    "result":{
        "status":0,
        "message":"ok",
        "request_id":"46e78874-3491-4a30-834e-98c0d76a1800",
        "sexyScore":0.2877,
        "pornScore":0.2183,
        "vulgarScore":0.1532,
        "normalScore":0.3409
    }
}
```






