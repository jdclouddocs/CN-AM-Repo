# 错误码

## 1.系统级错误码 
[详见返回码](https://aidoc.jd.com/user/returncode.html)  
## 2.业务错误码

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

