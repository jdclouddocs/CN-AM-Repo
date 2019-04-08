## 错误码

### 1.系统级错误码
[详见返回码](https://aidoc.jd.com/user/returncode.html)  

### 2.业务错误码 

<table>
   <tr>
      <th>业务错误码（status）</th>
      <th>message</th>
      <th>说明</th>
   </tr>
   <tr>
      <td>12002</td>
      <td>not enough param</td>
      <td>参数缺失（未传入任何图片）</td>
   </tr>
   <tr>
      <td>12003</td>
      <td>image type error</td>
      <td>解析参数错误,图片格式不支持</td>
   </tr>
   <tr>
      <td>12004</td>
      <td>image size exceeds 2M <br>  
      image size must be between 256X256 and 4096X4096</td>
      <td>图像超过尺2M,或者图片尺寸不在支持范围内。两者共用一个错误码12004</td>
   </tr>
</table>