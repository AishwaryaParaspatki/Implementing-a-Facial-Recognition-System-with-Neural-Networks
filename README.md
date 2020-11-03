# A Real Time Facial Recognition System with Siamese Neural Networks (One shot learning)

Implemented a One Shot Siamese Neural Network for image classification.

Database: ORL Face database.

This repo contains 6 Jupyter Notebooks:
1. visualize_face.ipynb: It visualizes the images in the dataset as below
![Visualize](/images/Visualize.png)
![Visualize_subjects](/images/Visualize_subjects.png)
2. onboarding.ipynb: Captures a picture and prepares onboarding for facial recognition system.
3. siamese_nn.ipynb
4. face_detection.ipynb
5. face_recognition_system.ipynb
6. utils.ipynb
Used a Stump-based 24x24 discrete adaboost frontal face detector created by Rainer Lienhart.<br>

The One shot Siamese facial recognition system uses the Harr Cascade Classifier which consists of Harr features. Harr features are similar to the convolutional filters as they both detect geometrical representations in images. Harr features are handcrafted and detect eyes, nose and lips in human faces based on human knowledge.
I have used the Harr features to calculate the similarity metric by sliding them over every region in an image. Hence, the face detection part of the project does not use any neural network algorithm.<br>
The real time face recognition system should be scalable, fast and highly accurate with small amount of data. This edge is achieved by One Shot Learning: Neural networks that can learn to recognize any face using just a single training sample.<br>
One Shot Learning Steps:<br>
1. Retrieve the stored image captured while onboarding. This is the True Image
2. Capture a test image in the recognition system.
3. The One Shot Siamese Convolutional Neural Network work in parallel with both the Ture image and the Test image to extract features from the faces.
4. These features are mapped in a lower dimension feature space based on their similarity and a similarity measure is outputted.
5. Finally, Euclidean distnce is used to measure the difference between the 2 lower dimensional vectors.<br>
<br>
True image:<br>
![True_Image](/images/true_img.png)
<br>
Below are the output images of the system identifying my face:<br>
![Smile](/images/Smile.png) <br>
![Normal](/images/Normal.png) <br>
![Weird face](/images/Weird_face.png) <br>
![Laughter](/images/Laughter.png) <br>
<br>
System correctly not identifying my friend, Shardool as me: br<>
![Shardool](/images/Shardool.png)
