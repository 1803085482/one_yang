---
title: Gocv
categories: [gocv&&opencv]
comments: true
---

### 一、准备材料

ubuntu版本：20.04.5

gocv版本：0.29.0  

opencv版本：4.5.3

gcc/g++版本：9.4.0

```python
# gocv下载 运行 go get -u -d gocv.io/x/gocv 记得代理
```



### 二、开始安装

```python
# cd gocv.io/x/gocv 进入目录 gocv.io/x/gocv

# 在目录下执行

# make deps

# make download

# cd /tmp/opencv/opencv-4.5.3/ 进入opencv-4.5.3安装包

# vim CMakeLists.txt 

# 添加命令 include(FindIconv)

# mkdir build 创建build文件

# cd build 进入build文件

""" 执行cmake 
-D CMAKE_BUILD_TYPE=RELEASE
-D CMAKE_INSTALL_PREFIX=/usr/local                -D OPENCV_EXTRA_MODULES_PATH=
../../opencv_contrib-4.5.3/modules   
-D WITH_JASPER=OFF
-D BUILD_DOCS=OFF
-D BUILD_EXAMPLES=OFF
-D ENABLE_CXX11=ON
-D WITH_INF_ENGINE=OFF
-D WITH_QT=OFF
-D WITH_GTK=OFF               
-D WITH_FFMPEG=OFF 
-D WITH_CUDA=ON 
-D WITH_TIFF=OFF              
-D WITH_OPENJPEG=OFF         
-D WITH_WEBP=OFF 
-D WITH_QT=OFF 
-D WITH_PNG=ON                 
-D WITH_1394=OFF 
-D HAVE_OPENEXR=OFF 
-D BUILD_TESTS=OFF 
-D BUILD_PERF_TESTS=OFF 
-D BUILD_opencv_java=NO 
-D BUILD_opencv_python=NO 
-D BUILD_opencv_python2=NO 
-D BUILD_opencv_python3=NO 
-D BUILD_SHARED_LIBS=OFF 
-D OPENCV_GENERATE_PKGCONFIG=ON .. """

# apt-get update && apt-get install -y git sudo

# make -j8

# make install

# 测试

# 执行pkg-config --modversion opencv4出来路径即可




```



参考[文章](https://blog.orchidflower.cn/2020/12/18/How-to-build-static-binary-with-gocv/)

