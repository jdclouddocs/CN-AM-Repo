# 评论观点抽取

## 一、接口描述 
### 1. 功能描述  
  提取输入的评论的观点标签。


### 2. 接口使用
平台为每个API提供试用体验服务，您在AI市场选择“免费试用”规格下单后，即可开始体验业内领先的人工智能API服务。
免费试用服务具有调用量、QPS限制，如需更高性能的API服务，可以提交咨询工单，联系京东AI扩容购买。

在获得使用权限后，您可使用已经封装好的SDK/参照[接口鉴权](https://aidoc.jd.com/user/auth.html)规则进行相应开发，整体流程详见   [接入流程](https://aidoc.jd.com/user/flow.html)


## 二、请求说明

### 1. 接口地址 ：

```
https://aiapi.jd.com/jdai/commentTag
```

### 2. 请求方式：

https `post` aiapi.jd.com/jdai/commentTag

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

#### （2）header请求参数
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
      <td>Content-Type</td>
      <td>string</td>
      <td>是</td>
      <td>application/json</td>
      <td>表示请求JSON格式的文本信息</td>
   </tr>
</table>

#### （3）body请求参数
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
      <td>text</td>
      <td>string</td>
      <td>是</td>
      <td>快递一共花了十七天才到</td>
      <td>输入文本</td>
   </tr>
</table>

### 4、请求代码示例
建议您使用我们提供的SDK进行调用，SDK获取及调用方式详见本页一接口描述中的2接口使用


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
      <td>参照四、错误码-业务错误码</td>
   </tr>
      <tr>
      <td>message</td>
      <td>string</td>
      <td>ok</td>
      <td>参照四、错误码-业务错误码</td>
   </tr>
      <tr>
      <td>request_id</td>
      <td>string</td>
      <td>5893465d31284468a8014de6ee430f8e</td>
      <td>便于双方定位问题</td>
   </tr>
   <tr>
      <td>commentTagList</td>
      <td>list</td>
      <td> [{"sentiment": 1, "property": "物流"},,...] </td>
      <td>观点信息，详情下面commentTagList字段说明</td>
   </tr>
</table>

#### commentTagList字段说明
<table>
   <tr>
      <th>名称</th>
      <th>类型</th>
      <th>示例值</th>
      <th>描述</th>
   </tr>
   <tr>
      <td>sentiment</td>
      <td>int</td>
      <td>1</td>
      <td>情感：0 积极，1 消极</td>
   </tr>
   <tr>
      <td>properity</td>
      <td>String</td>
      <td>物流</td>
      <td>属性 例如：物流，服务，功能等509种</td>
   </tr>
</table>


### 2、返回示例


```
{
    "code": "10000",
    "charge": false,
    "remain": 97,
    "msg": "查询成功",
    "result": {
                  "status": 0,
                  "request_id": "1c841e13-f2fb-4b60-966d-e9f7713de2e1",
                  "message": "ok",
                  "commentTagList": [
                      {
                          "sentiment": 1,
                          "property": "物流"
                      }
                  ]
              }
}
```

