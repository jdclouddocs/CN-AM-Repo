# 删除分组

----------

## 一、接口描述 

### 1.功能描述

删除一个人脸分组

### 2. 接口使用 
使用接口前，需要先完成API的下单购买，然后可使用已经封装好的SDK/参照[接口鉴权](https://aidoc.jd.com/user/auth.html)规则进行相应开发，整体流程详见   [接入流程](https://aidoc.jd.com/user/flow.html)  

## 二、请求说明

### 1. 接口地址 ：

```
https://aiapi.jd.com/jdai/faceGroupDelete
```

### 2. 请求方式：
  
https `post` aiapi.jd.com/jdai/faceGroupDelete

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
      <td>分组名称,若groupId不为空则以groupId作为删除分组的唯一标识</td>
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
      <td>若status为0，返回分组id，否则返回错误信息</td>
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
            "message": "8b94af03-67d7-47ec-ae56-bc5d50333076",
            "status": 0
    }
}
```
## 四、错误码

### 1.系统级错误码
[详见返回码](https://aidoc.jd.com/user/returncode.html)  

### 2.业务错误码 

<table>
   <tr>
      <th>业务错误码（status）</th>
      <th>对应message说明</th>
      <th>说明</th>
   </tr>
   <tr>
      <td>12002</td>
      <td>"groupId, groupName is null"</td>
      <td>参数缺失，分组名称和分组ID不能都为空</td>
   </tr>
   <tr>
      <td>13312</td>
      <td>"groupId not found"</td>
      <td>分组不存在，需要搜索的组的Id不存在，或者当搜索组Id为空但是分组名称不存在时会报该错误</td>
   </tr>
</table>