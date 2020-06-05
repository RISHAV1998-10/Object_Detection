# Object_Detection
Here goes the code for object detection
# Object detection using deep learning with OpenCV and Python 

OpenCV `dnn` module supports running inference on pre-trained deep learning models from popular frameworks like Caffe, Torch and TensorFlow. 

When it comes to object detection, popular detection frameworks are
 * YOLO
 * SSD
 * Faster R-CNN
 
 Support for running YOLO/DarkNet has been added to OpenCV dnn module recently. 
 
 ## Dependencies
  * opencv
  * numpy
  
`pip install numpy opencv-python`

**Note: Compatability with Python 2.x is not officially tested.**

 ## YOLO (You Only Look Once)
### Weights 
 Download the pre-trained YOLO v3 weights file from this [link](https://pjreddie.com/media/files/yolov3.weights) and place it in the current directory or you can directly download to the current directory in terminal using
 
 `$ wget https://pjreddie.com/media/files/yolov3.weights`
### Labels
  The yolov3.txt contains the labels of all the 80 classes
## Building Network
  The network is being build using the config(.cfg) file provided by the author
  We shall use pytorch to build our own network from scratch.
  The `DNMmodel.py` and `utils.py` are the files responsible for conversion
  
  The OpenCV version of this conversion is : `cv2.dnn.readNet` <br>
  The arguments to this function is (config,weights) which are `yolov3.cfg` and `yolov3.weights` respectively
 
