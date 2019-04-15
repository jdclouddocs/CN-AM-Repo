
# 错误码

### 1. 系统级错误码

<table>
  <tr>
    <th>返回码 (code)</th>
    <th>说明（message）</th>
  </tr>
    <tr>
      <td>10000</td>
      <td>查询成功</td>
    </tr>
  <tr>
    <td>10001</td>
    <td>错误的请求appkey</td>
  </tr>
  <tr>
    <td>10003</td>
    <td>不存在相应的数据信息</td>
  </tr>
  <tr>
    <td>10004</td>
    <td>URL上appkey参数不能为空</td>
  </tr>
    <tr>
      <td>10010</td>
      <td>接口需要付费，请充值</td>
    </tr>
   <tr>
    <td>10020</td>
    <td>系统繁忙，请稍后再试</td>
  </tr>
   <tr>
    <td>10030</td>
    <td>调用网关失败，请与NeuHub联系</td>
  </tr>
   <tr>
    <td>10040</td>
    <td>超过每天限量，请明天继续</td>
  </tr>
   <tr>
    <td>10041</td>
    <td>URL上timestamp参数不能为空</td>
  </tr>
   <tr>
    <td>10042</td>
    <td>URL上sign参数不能为空</td>
  </tr>
   <tr>
    <td>10043</td>
    <td>超过QPS限额，请降低调用频率或与NeuHub联系</td>
  </tr>
  <tr>
    <td>10044</td>
    <td>集群QPS超限额，请与NeuHub联系</td>
  </tr>
  <tr>
    <td>10045</td>
    <td>timestamp参数无效，请检查timestamp距离当前时间是否超过5分钟</td>
  </tr>
  <tr>
    <td>10046</td>
    <td>timestamp参数格式错误</td>
  </tr>
  <tr>
    <td>10047</td>
    <td>请求签名sign无效，请检查签名信息</td>
  </tr>
  <tr>
    <td>10048</td>
    <td>无接口权限，请下单购买</td>
  </tr>
  <tr>
    <td>10050</td>
    <td>用户已被禁用</td>
  </tr>   
  <tr>
    <td>10060</td>
    <td>发布方设置调用权限，请联系发布方</td>
  </tr>
  <tr>
    <td>11010</td>
    <td>发布方接口调用异常，请稍后再试</td>
  </tr>
  <tr>
    <td>11030</td>
    <td>发布方接口返回格式有误</td>
  </tr>  
</table>  

### 2.业务错误码 

<table>
   <tr>
      <th>业务错误码（status）</th>
      <th>对应message说明</th>
      <th>说明</th>
   </tr>
   <tr>
      <td>12002</td>
      <td>"groupId, groupName is null, or outerId is null"</td>
      <td>参数缺失，分组名称和分组ID不能都为空，outerId不能为空</td>
   </tr>
   <tr>
      <td>13312</td>
      <td>"groupId not found"</td>
      <td>分组不存在，需要搜索的组的Id不存在，或者当搜索组Id为空但是分组名称不存在时会报该错误</td>
   </tr>
   <tr>
   		<td>13320</td>
   		<td>"outerId not found"</td>
   		<td>人脸ID不存在，用户指定的搜索的组的名称的人脸分组里，若不存在用户指定需要删除ID对应的人脸会报该错误</td>
   </tr>
</table>