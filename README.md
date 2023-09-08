# Weapon-Detection
## A SSD Model for Weapon Detection

- To produce detections of different scales, the SSD network uses feature maps from different layers of a modified VGG16 networks.
- The changes made to the VGG16 network includes:
  - The fc6 and fc7 of VGG16 is turned into convolutional layers through the use of Atrous Convolution.
  - The pool size of pool5 is changed from (2, 2) to (3, 3) with strides of (1, 1).
  - L2 Normalization is added to conv4_3 of the VGG16 network. The network is then extended with SSD’s extra feature layers.
- Since each feature map item corresponds to different locations/patches in the original image, the feature maps at the beginning of the network allows for detections of small objects while those at the end of the network allows for detections of large objects.
- The feature maps used to construct SSD300 with VGG16 base network are: conv4_3, fc7, conv8_2, conv9_2, conv10_2 and conv11_2.

![Screenshot from 2023-09-08 22-39-45](https://github.com/Sanskritiq/Weapon-Detection/assets/72336465/50e437bc-ef48-4f68-9c0b-a0d616de5cdd)


#### [Presentation link](https://www.canva.com/design/DAE_qBysVXY/mfxukzczQb0m-84ZjJFk7A/view?utm_content=DAE_qBysVXY&utm_campaign=designshare&utm_medium=link&utm_source=homepage_design_menu)


###### Note:- 'Socret360/object-detection-in-keras'  was used as reference
