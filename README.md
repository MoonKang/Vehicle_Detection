# Vehicle Detection

Goals:
* Perform a Histogram of Oriented Gradients (HOG) feature extraction on a labeled training set of images and train a classifier Linear SVM classifier
* Optionally, you can also apply a color transform and append binned color features, as well as histograms of color, to your HOG feature vector. 
* Note: for those first two steps don't forget to normalize your features and randomize a selection for training and testing.
* Implement a sliding-window technique and use your trained classifier to search for vehicles in images.
* Run your pipeline on a video stream (start with the test_video.mp4 and later implement on full project_video.mp4) and create a heat map of recurring detections frame by frame to reject outliers and follow detected vehicles.
* Estimate a bounding box for vehicles detected.

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

####1. Feature Extraction - 

![alt text][image4]
![alt text][image5]

####2. Build Vehicle Classifier
![alt text][image6]

####3. Window Search
![alt text][image7]

####Output
![alt text][image8]
