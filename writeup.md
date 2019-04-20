# **Finding Lane Lines on the Road** 

The goal of this project is to produce lane lines on the roads of the california
highway make it suitable it in such a way that the project is suitable for a self driving car to move in a particular lane of the road



### 1. Describe your pipeline. As part of the description, explain how you modified the draw_lines() function.

My Pipeline consisted of the following steps
1. First the conversion of the image to grayscale was done so that the edges from the images can be found using the canny edge detection.
2. Then gaussian blurr function to remove the noise from the image for the better detection of edges using canny.
3. The edges using the canny edge detection was done and it's parameters were taken in the ratio of 1:2 for the better identification of edges.
 4. Now the edges in the whole image were identified and but our use is basically of the edges ofr the lanes of the road so using the regio of interest unction the edges of other part of the image were removed.
 5. Then the Hough Transformation was done which helped in getting extracting the segments of lines from the edges of the image.
 6. Now the line segments from the Hough Transformation were converted by the lane_lines function which was used to make the complete line and also differentiating between line segments based on the slope of the line.
 7. Now the images were combined such that lanes are identified on the original image using the weighted_image function. 



If you'd like to include images to show how the pipeline works, here is how to include an image: 


### 2. Identify potential shortcomings with your current pipeline


One potential shortcoming would be what would happen when there are large turns i.e it the lane_lines function could be modified as the lanes were not that properly identified to a 100% accuracy. 


### 3. Suggest possible improvements to your pipeline

A possible improvement would be to make sure on the large turns the lane line function could be automated in such a way that there is no problems for the future use of it and thresholds for the slope could be adjusted for the kind of road



