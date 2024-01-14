# LeafGAN Replication
A Semi-Replication of LeafGAN for Sick Leaves Identification

This is a project for the course of Deep Learning at Istanbul Technical University. The project aims to replicate the LeafGAN project on our own datasets. 1 of the datasets is for cucumber leaves while the other is for tomato leaves. The cucmber leaves were a combination of images collected via the internet and some images from a dataset (comes from an uncontolled environment), and the tomato leaves come completely from a controlled domain envirnoment dataset

1- Since we have 2 datasets. You can try the demo by either accessing the PlantProject directory (original trial with the gathered cucmber leaves images) or with the PlantProject - Tomatoes directory for the 2nd and 3rd trials on datsets gathered from a dataset found on the internet referenced in the report.  

(The renaming has been already done so there will be no need to check the functionality of the file)

1- Splitting and Labelling of data: you should first try the splitting and labelling of data jupyter file in the directory. The file works even if the images and labels already exist but does not replicate the copying of the images and labels.

2- The training of LFLSeg: you can then train the LFLSeg model (path in the directories: LeafGAN-master\LFLSeg\train_LFLSeg.py) simply by running the code via any IDE (Pycharm).

3- LFLSeg could then be tested on indiviidual pictures by first uploading the model to the infer_LFLSeg.py file on line 84 by modifying the path of the saved trained LFLSeg model. We should navigate to the directory (PlantProject\LeafGAN-master\LFLSeg) from conda terminal and run:

  python infer_LFLSeg.py  --input images/leaf_01.jpg --threshold 0.35 --segment
  or
  python infer_LFLSeg.py  --input images/leaf_01.jpg --threshold 0.35

  Note the differnce between the 2 is that the first produces a masked picture but without a heatmap segmentation. The 2nd produces a heatmap segmentation. The produced files are saved in the output folder inside the LFLSeg directory. A model has been already uploaded to the infer_LFLSeg.py file.

4- 
