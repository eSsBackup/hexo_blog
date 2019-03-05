---
title: Tensorflow Configuration
date: 2018-07-29 13:05:37
tags:
---
- ImportError: libcusolver.so.8.0: cannot open shared object file: No such file or directory
  Failed to load the native TensorFlow runtime.

  - 解决：在edit configurations中配置python运行环境变量，添加LD_LIBRARY_PATH，设置路径/usr/local/cuda/lib64

  ```bash
	source activate tf
  ```