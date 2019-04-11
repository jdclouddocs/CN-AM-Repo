# 错误码

### 1.系统级错误码 
[详见返回码](https://aidoc.jd.com/user/returncode.html)  
### 2.业务错误码

业务错误码（code）|对应message|说明
------|------|------
12001|File was missing or 0 bytes|图片缺失或者为空
12002|File error|文件读取出错
12003|File format only allow: jpg(jpeg), png|图片格式只支持jpg(jpeg),png两种
12004|The file size is too large. Maximum supports 5M|文件太大，最多支持5M
12005|Recognize Error|识别出错
12006|Program Error|程序内部错误
12007|Recognize empty result|识别结果为空