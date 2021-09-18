Key Points:-

1. Steps involved:

(i) Detect the objects in the image and calculate their centroids.
(ii) Find out the previous occurrence of that all those objects using euclidean distance. Some objects might be new and some might have gone out of frame.
(iii) Track the objecs as it moves around in the video and print the associated id with them.
2. Assumptions:
(i) The object detection part is not built here. It should have been built previously. We take the face detection deep learning model here to detect faces.
(ii) The objects don't move too fast in the video.
(iii) The object moves in the frame but the distance between the centroids in the current and next frame is smaller than all other distances between objects.
3. This approach is based on Centroid tracking.
4. Euclidean distance is used to calculate the distance between new objects detections and previous ones.
5. The smaller the euclidean distance of new object to the old object, the more are the chances of it being the same old object.
6. Video stream from webcam is used in this project to do object tracking.
7. OpenCV's deep learning based face detector is used to detect faces.

Requirements:-

python (3.7.3)
opencv (4.1.0)
imutils (0.5.2)

Limitations:-

1. The centroid tacking algorithm requires that the centroids must lie close together between subsequent frames.
2. There could be object id switching if the objects overlap each other.
