
# 错误码

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
      <td>正常返回</td>
   </tr>
   <tr>
      <td>1001</td>
      <td>only post method is allowed</td>
      <td>错误的访问方法，仅支持post请求</td>
   </tr>
   <tr>
      <td>1002</td>
      <td>parameter error, "image" is required</td>
      <td>缺少必要参数</td>
   </tr>
   <tr>
      <td>1003</td>
      <td>invalid image base64 data</td>
      <td>base64图像解析失败</td>
   </tr>
   <tr>
      <td>1004</td>
      <td>incorrect image size</td>
      <td>图像大小超过限制</td>
   </tr>
   <tr>
      <td>1005</td>
      <td>not valid json string</td>
      <td>非法的json字符串</td>
   </tr>
   <tr>
      <td>1006</td>
      <td>other error</td>
      <td>其他错误</td>
   </tr>
</table>