# Bilateral filter

## 1. 环境

```yaml
cmake: 3.19.8
gcc/g++: 7.5.0
OpenCV: 4.5.2
CUDA: 10.0
```



## 2. Sample

```shell
sh run.sh
```


如果要换成 cuda 程序，只需要修改以下几行

```cmake

# CUDA
find_package(CUDA REQUIRED)
set(CUDA_NVCC_FLAGS -G;-g)

# 生成 cuda 可执行文件
cuda_add_executable(executor src/bilateral_filter.cu)

# add_executable(executor src/bilateral_filter.cpp)

```

结果如下：

[时间对比]



从左到右分别是：含噪声原图、CPU 双边滤波、GPU 双边滤波、CPU 高斯滤波

![image-20210621223918870](images/woman_2_comparison.png)

![image-20210621223929970](images/woman_1_comparison.png)



## 3. 原理



## 4. 实现



## 5. cuda 实现





