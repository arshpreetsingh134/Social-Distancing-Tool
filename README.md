# Social-Distancing-Tool
Social Distancing Tool using OpenCV &amp; Detectron2 (a FAIR library for Object Detection and Segmentation)

The project was tested on a demo video uploaded on YouTube, that was obtained from TRIDE (University of Oxford).
Link: https://www.youtube.com/watch?v=pk96gqasGBQ

I used Faster R-CNN Object Detection Algorithm and the weights of the COCO dataset which are easily available online.

This code was written on [Google Colab.](https://colab.research.google.com/) I would recommend using the same. *Change the runtime to GPU prior to installing the libraries.*


## Here is the algorithm:-

![alt text](https://github.com/arshpreetsingh134/Social-Distancing-Tool/blob/master/Faster%20R-CNN.jpg?raw=true "Faster R-CNN")

1. Load an Image.
2. Pass it through CNN.
3. Extract the features.
4. Select ROI (Region of Interest) features using Region Proposal Network(RPN).
5. For each ROI feature, pass features to a classifier (person or not?) & regressor (parameters for bounding box).

Unlike Fast R-CNN, which uses **exterior region proposal algorithm** (which extracts the regions that are likely to contain the object), Faster R-CNN uses a state-of-the-art **Region Proposal Network (RPN)**, which learns to propose the region of interests on its own, which in turn saves a lot of time and computation as compared to a Fast R-CNN.

*Faster R-CNN takes close to 0.2 seconds for every test image during inference and is about 250 times faster than Fast R-CNN.*
