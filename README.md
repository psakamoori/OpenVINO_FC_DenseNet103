# OpenVINO App for Image Semantic Segmentation using FCDenseNet103 

OpenVINO based FC-DenseNet-103 Image Semantic Segmentation with single/multi device (heterogenous) inference on Intel Powered  Edge device. 

# Pre-requisites
   1. Ubuntu 16.04/18.04 machine with OpenVINO 2020.R1/R2 with python3
   2. Intel Powered Edge device with CPU/iGPU/VPU (HDDL, NCS2)
   3. For Training: Tensorflow 2.2, Keras
  
# Running OpenVINO Model Optimizer for IR files

  1. Convert keras h5 to tensorflow pb 
  2. OpenVINO Model optimizer for IR files
     Ex: python3 mo_tf.py --input_model /home/psakamoori/MyProjects/FC-Densnet-103/100-tiramisu-keras/models/tiramisu.pb --date-type FP32 --input_shape [1,224,224,3]
  3. Run inference on test_image0.png 
     on CPU:
     python3 run_tiramisu_ir_camvid.py -m  ./models/tiramisu.xml -i images/test_image0.png -d CPU --labels ./camvid-master/label_colors.txt
