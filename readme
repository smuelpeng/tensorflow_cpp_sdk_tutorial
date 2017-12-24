# tensorflow_cpp_sdk_tutorial

总结高效使用tensorlow SDK的方式

## 主要功能

- 收集了使用tensorflow读取和写出图片的函数
- 实现tensorflow实现人脸图像超分辨率的SDK


![](http://github.com/smuelpeng/tensorflow_cpp_sdk_tutorial/raw/master/imgs/ori.jpg)
![](http://github.com/smuelpeng/tensorflow_cpp_sdk_tutorial/raw/master/imgs/output.jpg)

## 总体思路


## 编译和使用方法

首先安装bazel，按照官网步骤安装即可，哪种方式都可以
然后下载tensorflow源码
git clone https://github.com/tensorflow/tensorflow.git --recursive
将sdk复制到tensorflow/cc/目录下，改名为faceall，
分别运行
bazel build -c dbg --copt="-fPIC"  //tensorflow/cc/faceall:faceall
bazel build -c dbg --copt="-fPIC"  //tensorflow/cc/faceall:test_faceall
在 bazel/bin目录下tensorflow/cc/faceall目录下即可生成动态库和测试的test_faceall文件

在运行test_faceall前需要将模型和图片放到相应目录

