# Hand Gesture Recognition and Modification
## The Model
- This model _(Model_4_classes.h5)_ has been trained to detect 4 classes of objects: Paper, Rock, Scissors and Nothing (in case of none of them) using transfer learning on the InceptionV3 model till layer ‘mixed7’, followed by a Dense layer with 256 nodes (RelU), and a softmax layer with 4 output nodes using Keras with Tensorflow backend. 

- It was trained using the RMSprop optimizer with a batch size of 32 for 100 epochs. Input size of the images were (150, 150, 3). The images were rescaled and augmented before training. _(TrainInception_4classes.ipynb)_

- The dataset we used was a combination of images from the [rock-paper-scissors repository by Alessandro Giusti](https://github.com/alessandro-giusti/rock-paper-scissors/tree/master/datasets/final) and photographs clicked by each of our team members, and consisted of 1791 images in the training set and 654 images in the validation set.

- The final trained model resulted in an accuracy of 97.05% on the test set with 237 images.

- [Plot of training and validation accuracy versus the number of epochs.](https://drive.google.com/file/d/1icTGo5AldnyNEkTA-ejK2UIKDOVHnYJD/view?usp=sharing)

- [Plot of training and validation loss versus the number of epochs.](https://drive.google.com/file/d/14EKIrOiv1DzNoDQWFEBZ5daXIuKBsPUI/view?usp=sharing)

## Visualizing the model
- The model can be visualized using the file Visualize_4_classes.py.

- Uses OpenCV library and the webcam to do the same.

- Each frame is flipped, resized to 150x150 and then normalized before feeding into the network to make a prediction. 

- The program can be quit by hitting ‘Q’.

**Note:**
- The software requirements are listed in the _requirements.txt_ file.
- The model gives the best performance when used with a plain background.
