# Vehicle Detection

Goals:
* Perform a Histogram of Oriented Gradients (HOG) feature extraction on a labeled training set of images and train a classifier Linear SVM classifier
* Optionally, you can also apply a color transform and append binned color features, as well as histograms of color, to your HOG feature vector. 
* Note: for those first two steps don't forget to normalize your features and randomize a selection for training and testing.
* Implement a sliding-window technique and use your trained classifier to search for vehicles in images.
* Run your pipeline on a video stream (start with the test_video.mp4 and later implement on full project_video.mp4) and create a heat map of recurring detections frame by frame to reject outliers and follow detected vehicles.
* Estimate a bounding box for vehicles detected.

Process:
1. Feature Extraction - color, spatial binning, gradient, 
2. Build Vehicle Classifier
3. Window Search
4. 

[image]: ./output_images/colorspace_feature.png
[image1]: ./output_images/HOG_feature.png
[image2]: ./output_images/normalized_features.png
[image3]: ./output_images/windowsearch.png
[image4]: ./output_images/final.png

####1. Feature Extraction - 

![alt text][image]
![alt text][image1]

####2. Build Vehicle Classifier
![alt text][image2]

####3. Window Search
![alt text][image3]

####Output
