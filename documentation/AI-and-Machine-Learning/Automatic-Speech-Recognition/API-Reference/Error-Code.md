 
## 错误码

### 1. 系统级错误码
[详见返回码](https://aidoc.jd.com/user/returncode.html) 

### 2. 业务错误码

<table>
  <tr>
    <th>业务错误码（status）</th>
    <th>说明（message）</th>
  </tr>
  <tr>
    <td>0</td>
    <td>/</td>
  </tr>
  <tr>
    <td>31001</td>
    <td>语音数据为空</td>
  </tr>
  <tr>
    <td>31002</td>
    <td>语音数据过长，一次请求音频不能超过一分钟</td>
  </tr>
   <tr>
    <td>31003</td>
    <td>请求参数出错，缺少Request-Id、Sequence-Id或Application-Id等。</td>
  </tr>
   <tr>
    <td>31004</td>
    <td>音频头部格式解析错误</td>
  </tr>
   <tr>
    <td>31005</td>
    <td>音频采样率或通道数错误</td>
  </tr>
   <tr>
    <td>31006</td>
    <td>音频格式错误</td>
  </tr>
   <tr>
    <td>32001</td>
    <td>服务内部音频解码错误</td>
  </tr>
   <tr>
    <td>32002</td>
    <td>服务内部am-server模块错误</td>
  </tr>
  <tr>
    <td>32003</td>
    <td>服务内部链接decoder-server模块错误</td>
  </tr>
   <tr>
    <td>33001</td>
    <td>服务内部decoder-server模块错误</td>
  </tr>
   <tr>
    <td>33002</td>
    <td>服务内部语音识别解码失败</td>
  </tr>
</table>

