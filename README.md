# Faster RCNN
- **Author:** LomHoyum
- **Data:** 03/05/2020
- **Version:** 1.0.0
- **Brief:** A Faster RCNN complemented with TensorFlow.

---

## Test Environment
- **OS Environ**
`Ubuntu 16.04.5 `
`GPU: TITAN X (Pascal)`
`Anaconda 4.8.2`
`CUDA 10.2`
- **Dependencies**
`python 3.6.10`
`tensorflow-gpu 1.15.0`
`numpy 1.18.1`
`Pillow 5.3.0`


---

## Usage
1. Download `VOC2007` dataset with following instructions.
    ```Shell
    wget http://host.robots.ox.ac.uk/pascal/VOC/voc2007/VOCtrainval_06-Nov-2007.tar
	wget http://host.robots.ox.ac.uk/pascal/VOC/voc2007/VOCtest_06-Nov-2007.tar
	wget http://host.robots.ox.ac.uk/pascal/VOC/voc2007/VOCdevkit_08-Jun-2007.tar
    ```
2. Extract all of these tars into one directory named `VOCdevkit`.
    ```Shell
    tar xvf VOCtrainval_06-Nov-2007.tar
    tar xvf VOCtest_06-Nov-2007.tar
    tar xvf VOCdevkit_08-Jun-2007.tar
    ```
3. Set data at the correct path of `Faster RCNN` project.
    ```Shell
    mv $VOCdevkit $Faster-RCNN/data/VOCdevkit2007
    ```
4. Download pre-trained ImageNet `VGG16` model.

    ```Shell
    cd $Faster-RCNN/model/pretrained
    wget http://download.tensorflow.org/models/vgg_16_2016_08_28.tar.gz
    tar xvf vgg_16_2016_08_28.tar.gz
    rm vgg_16_2016_08_28.tar.gz
    ```
    
5. It should have this basic structure.
    ```
    Faster RCNN
        |──data
        |    |──VOCdevkit2007
        |    |    |──VOCcode
        |    |    |──VOC2007
        |    |    └──···
        |    └──···
        |──model
        |    └──pretrained
        |        └──vgg_16.ckpt
        |──network
        |    └──···
        |──train.py
        └──test.py
    ```
6. Train Faster RCNN with `Pascal VOC 2007`.
    ```Shell
    python3 train.py
    ```
7. Test.
    ```Shell
    python3 test.py
    ```
    
---

## Results
