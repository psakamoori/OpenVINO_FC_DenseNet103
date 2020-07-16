# OpenVINO Image Semantic Segmentation inference app for FCDenseNet103 

OpenVINO based Semantic Segmentation using FC DenseNet 103 


# Running OpenVINO Model Optimizer for IR files

  ### 1. Convert keras h5 to tensorflow pb 
  ### 2. OpenVINO Model optimizer for IR files
     Ex: python3 mo_tf.py --input_model /home/psakamoori/MyProjects/FC-Densnet-103/100-tiramisu-keras/models/tiramisu.pb --date-type FP32 --input_shape [1,224,224,3]
  ### 3. Run inference on test_image0.png 
     on CPU:
     python3 run_tiramisu_ir_camvid.py -m  ./models/tiramisu.xml -i images/test_image0.png -d CPU --labels ./camvid-master/label_colors.txt
