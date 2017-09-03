# Vehicle Detection

Goal:
* Estimate a bounding box for detected vehicle .

Process:
1. Color Feature
2. Histogram of oriented gradients(HOG) Feature
3. Build Vehicle Classifier
4. Window Search

[image4]: ./output_images/colorspace_feature.png
[image5]: ./output_images/HOG_feature.png
[image6]: ./output_images/normalized_features.png
[image7]: ./output_images/windowsearch.png
[image8]: ./output_images/final.png
#### Output
The final output comes out to be:
![alt text][image8]

#### 1. Feature Extraction - Color, HOG
1] As cars tend to have stronger Saturation values from HSV color space than non-cars, I have used its color values as part of feature.

![alt text][image4]

2] The idea behind HOG feature is to identify shape of gradients by blocks in a given channel of image. Through HOG extraction, we are interested in distinguishing a car image from a non-car by looking at its edges. 'get_hog_features' takes input of image, number of orientations, and size of cell and block. HOG will aggregate cell values and determine the gradient for each block.

![alt text][image5]

#### 2. Build Vehicle Classifier
After extracting features from all data, I used SVM to train the features. Before training the data, the data was normalized using StandardScaler() from sklearn.preprocessing. Then these normalized data were splitted into train and test sets. (80% Training, 20% Test set). 

![alt text][image6]
I trained a linear SVM using LinearSVC from sklearn and got test Accuracy of SVC = 0.987. 

#### 3. Window Search
* Implement a sliding-window technique and use the trained classifier to search for vehicles in images.

With trained vehicle classifer, I would run classifier across pixels of image. First, I would get multiple detections for a car (image1). Then, I create a heatmap to count and draw a box with endpoints that fit those detections. (image 2, 3) Finally, I would draw the box on original image to output a clean outlook of vehicle detection. This method prevents false positives and multiple detections to be shown in image.
![alt text][image7]


