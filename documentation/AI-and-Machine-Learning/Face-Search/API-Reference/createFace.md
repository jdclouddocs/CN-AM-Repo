# 创建人脸

----------

## 一、接口描述 

### 1.功能描述

为一个已经创建的人脸分组增加一张人脸

### 2. 接口使用 

公测期间用户可以免费（0元）进行测试，根据[购买流程](http://neuhub.jd.com/ai/api/face/search)下单后，即可开始体验业内领先的人工智能API服务。公测期间服务具有调用量、QPS限制，如需更高性能的API服务，请联系客服扩容购买。

使用接口前，需要先完成API的下单购买，然后可使用已经封装好的SDK/参照[接口鉴权](https://aidoc.jd.com/user/auth.html)规则进行相应开发，整体流程详见   [接入流程](https://aidoc.jd.com/user/flow.html)  

### 3.图片要求

> 1. 图片格式：bmp, jpg, jpeg, png, jfif
> 2. 图片像素尺寸：最小 48\*48 像素，最大 4096\*4096 像素
> 3. 图片文件大小：小于2MB

## 二、请求说明

### 1. 接口地址 ：

```
https://aiapi.jd.com/jdai/faceCreate
```

### 2. 请求方式：
  
https `post` aiapi.jd.com/jdai/faceCreate

### 3. 请求参数  
 
#### （1）query请求参数  
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
      <td>groupId</td>
      <td>string</td>
      <td>否</td>
      <td>6979e9bd79b944b49e0d6e74079d5098</td>
      <td>分组Id</td>
   </tr>
   <tr>
      <td>groupName</td>
      <td>string</td>
      <td>否</td>
      <td>test</td>
      <td>分组名称,若groupId不为空则以groupId作为分组的唯一标识</td>
   </tr>
   <tr>
      <td>outerId</td>
      <td>string</td>
      <td>是</td>
      <td>futianyu</td>
      <td>用户定义的人脸唯一标识，支持中文</td>
   </tr>
   <tr>
      <td>imageBase64</td>
      <td>string</td>
      <td>是</td>
      <td></td>
      <td>图片的Base64编码</td>
   </tr>
</table>

### 4、请求代码示例
建议您使用我们提供的SDK进行调用，SDK获取及调用方式详见本页一接口描述中的2接口使用
 
## 返回说明

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
      <td>1000</td>
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
      <td>0</td>
      <td>返回结果，0表示成功，非0为对应错误号</td>
   </tr>
   <tr>
      <td>message</td>
      <td>string</td>
      <td>Success</td>
      <td>返回错误信息</td>
   </tr>
   <tr>
      <td>result</td>
      <td>string</td>
      <td>Success</td>
      <td>返回人脸唯一标识faceId</td>
   </tr>
</table>
 


### 2、返回示例

```Json
{
    "status": 0, 
    "charge": false,
    "remain": 97,
    "msg": "查询成功",
    "result": 
    {
    	    "requestid": "6979e9bd79b944b49e0d6e74079d5098",
            "message": "success",
            "status": 0,
            "result":"{faceId:"daf9e9bd79b944b49e0d6e74079d5098"}"
    }
}
```
