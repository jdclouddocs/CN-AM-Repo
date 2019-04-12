
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
      <th>对应message说明</th>
      <th>说明</th>
   </tr>
   <tr>
      <td>12002</td>
      <td>1. "missing param" 2.groupId or groupName is null</td>
      <td>参数缺失.  1. 缺失参数 2.分组ID和分组名称都为空，两者不能均为空</td>
   </tr>
   <tr>
      <td>12003</td>
      <td>1."image base64 is invalid"</td>
      <td>解析参数错误。 1.图像Base64编码错误</td>
   </tr>
   <tr>
      <td>13111</td>
      <td>""image quality is bad""</td>
      <td>图像尺寸或者质量不符合标准，当图像尺寸超过4096 * 4096或者小于48 * 48时会报该错误</td>
   </tr>
   <tr>
      <td>13112</td>
      <td>"face quality is not stardard"</td>
      <td>人像质量不符合标准，当人脸姿态过大，人脸摇头，歪头，点头的角度超过30度会报该错误</td>
   </tr>
   <tr>
      <td>13134</td>
      <td>"face not found"</td>
      <td>找不到人脸，当图像中无法检测到人脸时会报该错误</td>
   </tr>
   <tr>
      <td>13303</td>
      <td>"time out"</td>
      <td>超时错误，当服务端请求负载过多会报该错误</td>
   </tr>
   <tr>
      <td>13312</td>
      <td>"groupId not found"</td>
      <td>分组Id不存在，需要搜索的组的Id不存在时会报该错误</td>
   </tr>
</table>