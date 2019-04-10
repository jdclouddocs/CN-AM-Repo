
# 错误码

## 1.系统级错误码
[详见返回码](https://aidoc.jd.com/user/returncode.html)  

## 2.业务错误码
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