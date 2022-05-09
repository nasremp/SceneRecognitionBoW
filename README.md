# SceneRecognitionBoW
Overview:
We will perform scene recognition with three different methods. We will classify scenes into one of 15 categories by training and testing on the 15 scene database (Lazebnik et al. 2006).

Task: Implement three scene recognition schemes:

●	Tiny images representation (get_tiny_images()) and nearest neighbor classifier (nearest_neighbor_classify()).

●	Bag of words representation (build_vocabulary(), get_bags_of_words()) and nearest neighbor classifier.

●	Bag of words representation and linear SVM classifier (svm_classify()).

Implementation:
● Tiny Image:
Get_tiny_images was used to create the tiny image as an image
representation. The accuracy with KNN classifier has poor performance which is
about to 20%.

● KNN classifier:
When classifying a feature into a particular category, we find the closest training
example using the euclidean distance to measure how far the examples were,
and then give the test case the label of that nearest training example.

● Build vocabulary:
We used it to establish a vocabulary of visual words and cluster them. First we
get the hog descriptors and then we cluster them using the kmeans(to return the
cluster centroids).

● Bag of words:
After getting the vocab and clustering them, we represent the training and testing
images as histograms of visual words. First, we get the hog descriptors and use
the euclidean distance to measure which cluster the descriptor belongs. Then we
create a histogram of visual words for each image, and then normalizes the
histograms.

● Support vector machine:
We use linear classifier as a learning model to operate in the bag of feature
space. This space was partitioned and then the test cases can be catigorized
based on the side they fall in.
