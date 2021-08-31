# Multitask computer aided diagnosis of breast masses



In this page, a multitask computer aided diagnosis (CADx) framework is devised to investigate interpretability for classifying breast masses. We investigate interpretability in CADx with the proposed multitask CADx framework. 



![image_2018-11-28 23_07_21](https://user-images.githubusercontent.com/44894722/49157188-8942c880-f362-11e8-9719-e73f15ab3fde.png)




## Dependencies
* python 3.7.11
* numpy 1.20.3
* h5py 3.4.0
* pytorch 1.6.0
* Pillow 8.3.1
* scipy 1.6.2
* torchray 1.0.0.2
* torchvision 0.7.0
* opencv-python 4.5.3.56


## Pretrained Models
Due to upload limit of Github, this page does not include checkpoint files. Please send request email to seongyeop@kaist.ac.kr if the checkpoint files are needed.

## How to use
First, go into the 'data' directory and download "DDSM dataset"

For data consistency, mammograms scanned by Howtek 960 were selected from the DDSM dataset.
By using LJPEG2PNG tool "DDSMUtility", load breast image.
Preprocess the DDSM dataset to create a h5 file. It resizes images to 64*64.

After that preprecess the pretrained model vgg16_weights.npz

    cd preprocess
    python prepare.py

Finally, go into the 'code' directory and run 'main_ICADx.py'.
    
    cd ..
    python main_ICADx.py
    

You can see the samples in 'img and test' directory.


## Reference Code
https://github.com/trane293/DDSMUtility
