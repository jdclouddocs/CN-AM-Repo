
# 错误码

### 1. 系统级错误码
<table>
  <tr>
    <th>返回码 (code)</th>
    <th>说明（message）</th>
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
      <th>对应message</th>
      <th>说明</th>
   </tr>
  <tr>
    <td>0</td>
    <td>"ok"</td>
    <td>正常</td>
  </tr>
  <tr>
    <td>11001</td>
    <td>"invalid param"</td>
    <td>用户相关，参数错误</td>
  </tr>
  <tr>
    <td>30201</td>
    <td>"server err, invalid cntl"</td>
    <td>服务器相关， 服务器未完成初始化</td>
  </tr>
   <tr>
    <td>30202</td>
    <td>"server is busy now, call later"</td>
    <td>服务器相关， 服务器忙</td>
  </tr>
   <tr>
    <td>30203</td>
    <td>"text too short"</td>
    <td>用户相关，文本过短（没有文本时返回）</td>
  </tr>
   <tr>
    <td>30204</td>
    <td>"text too long"</td>
    <td>用户相关，文本过长（超过1024字节）</td>
  </tr>
   <tr>
    <td>30205</td>
    <td>"server err, error seqid"</td>
    <td>用户相关，seq_id不正确，如值为1但是当前已有相同session; 或值不为1但当前没有相同session</td>
  </tr>
   <tr>
    <td>30206</td>
    <td>"server err, read response failed"</td>
    <td>TTS引擎相关，TTS引擎读取错误</td>
  </tr>
   <tr>
    <td>30207</td>
    <td>"server err, base64 encode failed"</td>
    <td>base64编码失败</td>
  </tr>
</table>