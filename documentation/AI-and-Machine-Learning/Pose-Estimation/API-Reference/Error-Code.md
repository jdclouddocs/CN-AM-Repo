
# 错误码

## 1.系统级错误码
[详见返回码](https://aidoc.jd.com/user/returncode.html)  
## 2.业务错误码


<table>
   <tr>
      <th>业务错误码（status）</th>
      <th>message</th>
      <th>说明</th>
   </tr>
   <tr>
      <td>12001</td>
      <td>param 'muti_det' must be 1 or 2</td>
      <td>参数'muti_det'必须为1或者2</td>
   </tr>
   <tr>
      <td>12002</td>
      <td>not enough param</td>
      <td>参数缺失，muti_det参数未被获取到</td>
   </tr>
   <tr>
      <td>12002</td>
      <td>not enough param,an image is needed</td>
      <td>参数缺失，未传入图片，与上方情况共用一个错误码</td>
   </tr>
   <tr>
      <td>12003</td>
      <td>image type error</td>
      <td>解析参数错误,图片格式不支持</td>
   </tr>
   <tr>
      <td>12004</td>
      <td>image size exceeds 2M </td>
      <td>图片大小超过限制，图像超过2M</td>
   </tr>
   <tr>
      <td>12004</td>
      <td>image size must be between 256X256 and 4096X4096</td>
      <td>图片大小超过限制，图片尺寸不在支持范围内，与上方情况共用一个错误码</td>
   </tr>
</table>
