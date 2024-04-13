---
layout: post
title:  Accelerating VGG16 DCNN With An FPGA
---

VGG16 is a convolutional neural network model, which achieves 92.7% top-5 test accuracy on ImageNet. The objective of this project was to modify the VGG process flow to use our custom convolution layer, implemented on the AWS F1 FPGA.

On the software side we use PyTorch’s C++ Extension to add C++ host code to PyTorch and create a custom FPGA conv2d layer, for each convolution layer on the VGG16. We bind C++ functions to Python functions and use the forward function to call the OpenCL
host code, which then performs the required operations on the kernel. The output that is returned has been verified with the regular nn.conv2d operation, to make sure that they are indeed the same.

On the hardware side, we implement the convolution as a generalized matrix multiplication (GEMM). We utilize a 16x16 systolic array design with an accumulator for the matrix multiplication. To deal with the problem of large run times due to kernel data transfer, we modified the kernel to compute block matrix multiplication for one entire row of blocks in the filter matrix and a corresponding
one entire column of blocks in the image matrix. This leads to the generation of one row of block-elements in the resultant product matrix. Each element of the product matrix is written one-by-one to global memory. This cuts down the number of transfers made to the kernel by a significant extent for large matrices. To take full advantage of this modification, we have initialized
and used two compute units (2 CU’s) to work parallelly. One CU computes the products for one entire row of the filter matrix and one entire column of the image matrix, the second CU computes the product for the same row of the filter matrix and the adjacent column of the image matrix.

View the code -> [GitHub](https://github.com/rashmip98/accelerating-vgg16)

Read the report -> [Google Drive](https://drive.google.com/file/d/1_t-ZUs8Ksm7X3zX2y6vlzE8V9R8Q-tjK/view)
