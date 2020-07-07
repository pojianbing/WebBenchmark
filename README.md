# WebBenchmark
`WebBenchmark`是一款基于开源通讯组件`Beetlex`扩展的`Webapi`管理和性能测试工具，在传统工具中一般管理工具缺乏性能压测能力或有性能测试的缺少管理功能；`WebBenchmark`的设计目标是就管理和性能压测能力同时具备。接下来介绍一下工具的功能和使用：
## 功能
- 支持HTTP和HTTPS的服务测试
- 暂只支持基础方法的GET,POST,PUT和DELETE
- 支持多用户和多分类管理
- 提供访问API详细时间线信息
- 提供值函数支持，可以更好地进行随机性数据构建和压测
- 支持多用例同时压测
- 提供详细的响应状态和各延时汇总

## 安装
工具是基于`.netcore`开发，可以运行在安装有.net core 2.1或更高版本的各大平台上。可以到 https://gitee.com/ikende/WebBenchmark 下载最新版本的压缩包，根据不同平台运行`run.sh`或`run.bat`.工具默认占用80端口，如果存在端口被占用问题可以编辑以上两个文件修改对应启动端口。
启动后可以通过浏览器访问相关服务，初始的用户名和密码是:`admin`和`123456`.进入服务后工具界面如下：


![image](https://user-images.githubusercontent.com/2564178/86763474-f0197f00-c079-11ea-88ff-38a85ff279a4.png)


![image](https://user-images.githubusercontent.com/2564178/86763543-fc054100-c079-11ea-9e31-9e441d47678a.png)

## 新建用例
工具的首页面是基础用例管理，在这里可以添加、管理和测试webapi的用例 ;通过点击添加按钮可以新增一下基础的测试用例 



添加的信息主要包括有基础用例信息和相关HTTP请求内容描述。
- **地址参数**
 
  主要是包括在Url里面的参数，参数可以根据自己的需要来添加并设置.

参数值支持函数引用，通过函数即可以在每次请求的都产生新的函数值进行提交。

- **请求头**

  主要可以添加一些请求头信息，如token和User-agent等。
![输入图片说明](https://images.gitee.com/uploads/images/2020/0707/102243_36fbea90_1522909.png "屏幕截图.png")
  
- **请求内容**

  工具暂只支持`application/json`和`form-urlencoded`两种，工具还专门为json提供更简便和具备验证能力的编辑器方便录入
![输入图片说明](https://images.gitee.com/uploads/images/2020/0707/102248_8b98cbda_1522909.png "屏幕截图.png")

- **测试**

  组件在编辑的时候就对当前用例进行一个测试，通过测试可以了解到当前用例运行的实际情况(包括整个测试过程的一些网络请求响应时间线).
![输入图片说明](https://images.gitee.com/uploads/images/2020/0707/102255_a0acaadc_1522909.png "屏幕截图.png")

## 批量测试
工具支持单个或批量测试用例,只要选择相关用例进行批量测试即可

![输入图片说明](https://images.gitee.com/uploads/images/2020/0707/102300_bffb3dd0_1522909.png "屏幕截图.png")
批量测试完成后即可实时查看每个用例的测试情况和相关处理时间线。

## 性能测试
工具提供多用例组合性能测试，只需要在创建性能测试用例时选择需要压测的用例即可。

![输入图片说明](https://images.gitee.com/uploads/images/2020/0707/102306_0fc4c300_1522909.png "屏幕截图.png")
保存好相关性能测试用例即保存到相关列表中

![输入图片说明](https://images.gitee.com/uploads/images/2020/0707/102310_7520ea1f_1522909.png "屏幕截图.png")

这时候就可以点击相关用例测试按钮进入到性能测试页面

![输入图片说明](https://images.gitee.com/uploads/images/2020/0707/102317_2ef13129_1522909.png "屏幕截图.png")
这时候可以根据自己需求设置相关并发测试的数据进行一个压力测试。

![输入图片说明](https://images.gitee.com/uploads/images/2020/0707/102322_186918a5_1522909.png "屏幕截图.png")
工具在测试过程中实时反映当前压测的结果，并把相关状态和相应延时分布数据详细显示出来。如果想查看压测过程中某个请求的详细情况，可以点击相关用例 即可显示该用户的详细情况

![输入图片说明](https://images.gitee.com/uploads/images/2020/0707/102328_c7fea3b5_1522909.png "屏幕截图.png")


以上是工具使用的相关介绍，有些功能在免费版本中受限。想更多了解可以查看在线演示 http://webbenchmark.beetlex.io/

