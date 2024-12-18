# RockPaperScissors_CNN
* **Convolutional Neural Network** for Image Classification
* Use the 'rock_paper_scissors' dataset from tensorflow_datasets.
* Class labels <br>
  **0 = rock** <br>
  **1 = paper** <br>
  **2 = scissors** <br>
* Training data has 2,520 images that are 300 by 300 pixels. A preview of these are shown in training_images_preview.png.
* Testing data has 372 images that are 300 by 300 pixels.
* Training images are standardized by converting each to 32-bit floats and dividing by the maximum pixel intensity of 255. The same is done for the testing data for consistency.
* To use categorical crossentropy loss function, we use 'to_categorical' from tensorflow.keras.utils to perform one-hot-encoding. There are of course 3 classes, so this type of encoding yields a numpy array with a 1 in the column representing the correct hand motion and 0's everywhere else in that column.
* The Convolutional Neural Network alternates Conv2D and MaxPooling2D layers.
* Then, the results are flattened and dense layers allow for classification with the 'softmax' activation function.
* The images are printed with their predicted and actual classes below each image.
* Final testing accuracy is about 77%
* To gain insight about issues with classification, testing images that were misclassified are shown with the predicted and actual classifications in testing_misclass_preview.png.
* Check the wiki for full documentation with explanation and code alternating.
