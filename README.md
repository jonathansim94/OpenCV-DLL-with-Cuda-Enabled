# OpenCV DLL with Cuda Enabled

Yes, I am the random guy who can maybe save you. If you are looking for DLLs with CUDA enabled to use OpenCV you are in the right place.
Because yes, compiling these libraries is hell. I spent 3 days to make the build of the libraries correctly.

My use case is using them in OpenCV for Unity with CUDA for faster inference in motion tracking task (mediapipe):
https://assetstore.unity.com/packages/tools/integration/opencv-for-unity-21088

Refer to that link for more information:
https://github.com/EnoxSoftware/OpenCVForUnity/issues/179

To use them you should have the following dependencies installed (you can find all on NVIDIA website):
- CUDA 10.1
- CUDNN 8.0.5 (merge zip content into the CUDA folder)
- Nvidia Video Codec SDK 12.2 (apply for NVIDIA Developer Program to download it):
  - copy from lib/x64 nvcuvid.lib and nvencodedapi.lib to CUDA_FOLDER/v.10.1/lib/x64
  - copy also the headers from Interface folder to CUDA_FOLDER\v10.1\include)

 The libraries have been compiled for all supported GPU architectures.
 Tested on series 10, 20 and MX GPUs.
