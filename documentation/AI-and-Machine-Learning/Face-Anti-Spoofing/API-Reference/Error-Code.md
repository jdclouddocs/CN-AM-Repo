# 错误码

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
      <td>"missing param"</td>
      <td>参数缺失</td>
   </tr>
   <tr>
      <td>12003</td>
      <td>"image base64 is invalid"</td>
      <td>解析参数错误</td>
   </tr>
	 <tr>
      <td>13111</td>
      <td>""image quality is bad""</td>
      <td>图像尺寸或者质量不符合标准，当图像尺寸超过4096 * 4096或者小于48 * 48时会报该错误</td>
   </tr>
   <tr>
      <td>13303</td>
      <td>"time out"</td>
      <td>超时错误，当服务端请求负载过多会报该错误</td>
   </tr>
</table>