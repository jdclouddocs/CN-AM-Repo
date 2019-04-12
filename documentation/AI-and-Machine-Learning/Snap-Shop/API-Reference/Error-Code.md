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

业务错误码（status）|对应message|说明
------|------|------
1002|"Error Input!"|读取图像失败
1005|"Input size is bigger than 2M, Error Quit!"|图像过大
1006|"Input is too small, Error Quit!"|图像过小
20001|"Request Service Error!"|图像请求过程失败
20002|"Request Service Error!"|图像请求过程失败
20003|"Request Service Error!"|图像请求过程失败
20004|"Request Service Error!"|图像请求过程失败
20005|"Request Service Error!"|图像请求过程失败
20007|"CHANNELID IS NECESSORY!"|channel_id(用户识别码)不能为空
20008|"Channel_Id is not registered,please contact the administrator!"|未注册用户识别码，不予以提供服务
20011|"API is updating now. Your channel_id has been processed up to upper limit and can no longer be used today, please retry it tommorrow."| channel_id当日调用量超限
20012|"&#39;main_category_list=&#39; is Necessory !"|参数main_category_list缺失
20014|"&#39;action_type=&#39; must Be 0 or 1 !"|参数action_type值错误
20015|"&#39;main_body_rectangle=&#39; is Necessory !"|参数main_body_rectangle缺失
20016|"&#39;main_category_id=&#39; is Necessory !"|参数main_category_id缺失
20017|"&#39;channel_id=test&#39; Does not Support USER ACTION!"|测试接口不支持用户反馈请求
20018|"categoryId error or categoryList is not the response one!"|类目请求类别错误或者请求的类目列表错误

