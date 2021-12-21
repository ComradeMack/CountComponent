# CountComponent
Step 1: Apply threshold to the image for differentiating the background and the component object we are focusing 

Step 2: Apply opening morphology (erode then dilate) to the threshold image for focusing the component objects and 
preventing false component detection (or noise) we are not considering

Step 3: Use connected component algorithm to detect and count the focused components.

Step 4: Get the count from output[0]-1 (subtract the background count). In order to put the detection frame around 
each object, use cv2.rectangle and cv2.puttext to write each count number from centroids matrix that collect all 
origin points of all components.

# Remarks

You can use this template to develop more accurate detection for specific purposes. 
This is just an example for detecting spores of Pyricularia Oryzae.

# Requirements
Python 3.8

Opencv

Numpy

Matplotlib

# Further reading

Morphology (erode, dilate, opening, closing, etc.) - https://docs.opencv.org/3.4/d9/d61/tutorial_py_morphological_ops.html

Connected component - https://www.pyimagesearch.com/2021/02/22/opencv-connected-component-labeling-and-analysis/
