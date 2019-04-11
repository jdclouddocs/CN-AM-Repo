# 四、错误码

## 1.系统级错误码
[详见返回码](https://aidoc.jd.com/user/returncode.html)  
## 2.业务错误码


<table>
   <tr>
      <th>业务错误码（status）</th>
      <th>对应message说明</th>
      <th>说明（message）</th>
   </tr>
   <tr>
      <td>1000</td>
      <td>ok</td>
      <td>返回正常</td>
   </tr>
   <tr>
      <td>1001</td>
      <td>parameter error</td>
      <td>缺少某个必选参数</td>
   </tr>
   <tr>
      <td>1002</td>
      <td>not valid json string</td>
      <td>非法的json字符串</td>
   </tr>
   <tr>
      <td>1003</td>
      <td>base64 image flow failed</td>
      <td>base64图像解析失败</td>
   </tr>
   <tr>
      <td>1004</td>
      <td>incorrect image size</td>
      <td>图像大小超过限制</td>
   </tr>
   <tr>
      <td>1005</td>
      <td>not valid image format</td>
      <td>非法的图像格式</td>
   </tr>
   <tr>
      <td>1006</td>
      <td>only portrait image is allowed</td>
      <td>输入需是人像图片</td>
   </tr>
   <tr>
      <td>1007</td>
      <td>time out</td>
      <td>请求超时</td>
   </tr>
   <tr>
      <td>1008</td>
      <td>only post method is allowed</td>
      <td>只允许post请求</td>
   </tr>
</table>