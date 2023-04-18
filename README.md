
# Detail readme.md is coming soon 

# how to use

i will upload a onnx and some images for nuScenes-minni to text. wait few days.

pytorch to onnx

https://github.com/thfylsty/FastBEV
 
make bev -j8


protobuf releted libs are in third_party

just support Tensorrt8.x

(if you want to try Tensorrt7.x , refer to tensorRT_Pro replace the "onnx_parser" for trt7 )


# other  about timeseq

其实加入时序也很简单，

在plugin的workspace中划分一块空间保存前一帧的特征即可。

在pytorch2onnx 的时候，plugin-trt return 两个tensor出来传递给3D 卷积部分即可。

在c++  cu 的实现中，直接将结果保存到workspace中，下一次执行plugin直接return两个出去即可。

我这里暂时用不到所以没加入，仅提供思路。

有兴趣的佬们可以试试看。


below ↓ translate by google ahhhhhhh

Actually, adding timing is also very simple,

Divide a space in the plugin's workspace to save the features of the previous frame.

In Pytorch2Onnx, the plugin rt returns two tensors and passes them to the 3D convolution section.

In the implementation of C++cu, the results are directly saved to the workspace, and the next time the plugin is executed, two can be returned directly.

I am currently unable to use it here, so I did not join. I only provide ideas.

Big guys can give it a try.

# Reference:

TensorRT

https://github.com/shouxieai/tensorRT_Pro