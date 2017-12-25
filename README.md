# tensorflow_cpp_sdk_tutorial

总结高效使用tensorlow SDK的方式

## 主要功能

- 收集了使用tensorflow读取和写出图片的函数
- 实现tensorflow人脸图像超分辨率的SDK


![](http://github.com/smuelpeng/tensorflow_cpp_sdk_tutorial/raw/master/imgs/ori.jpg)
![](http://github.com/smuelpeng/tensorflow_cpp_sdk_tutorial/raw/master/imgs/output.jpg)

## 编译和使用方法

首先安装bazel，按照官网步骤安装即可，哪种方式都可以

然后下载tensorflow源码

git clone https://github.com/tensorflow/tensorflow.git --recursive

将sdk复制到tensorflow/cc/目录下，改名为faceall，分别运行

bazel build -c dbg --copt="-fPIC"  //tensorflow/cc/faceall:faceall

bazel build -c dbg --copt="-fPIC"  //tensorflow/cc/faceall:test_faceall

在 bazel/bin目录下tensorflow/cc/faceall目录下即可生成动态库和测试的test_faceall文件

在运行test_faceall前需要将模型和图片放到相应目录

## Todo
解决handle预先初始化不能运行的问题
解决位置无关的运行环境的问题

## 参考链接
读图片：

https://github.com/tensorflow/tensorflow/blob/master/tensorflow/examples/label_image/main.cc
https://github.com/tensorflow/models/issues/1741

存图片：

https://www.jianshu.com/p/b6f9451716ed?utm_campaign=maleskine&utm_content=note&utm_medium=seo_notes&utm_source=recommendation

模型转换：

http://blog.csdn.net/rockingdingo/article/details/75452711

bazel使用：bazel help 以及google各种网址都可以
