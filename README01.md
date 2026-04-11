Problem Set 01: Pneumonia Classification (CNN)
1. My Approach
For this assignment, I had to build a model that can look at a chest X-ray and decide if a patient has pneumonia or is healthy. I decided to use a Convolutional Neural Network (CNN) because it's the standard for image tasks. My goal was to create a model that is deep enough to catch the details in the lungs but not so complex that it takes too long to train or overfits.

2. How I Built the Model
I followed a few specific steps to make the model work better:

Preparing the Data: The original images were all different sizes, so I resized everything to 150x150. I also used Data Augmentation (like zooming and flipping the images). I did this because medical images can vary, and I wanted my model to be able to recognize pneumonia even if the X-ray was slightly angled or zoomed in.

The Architecture: * I used three layers of convolutions to pick up on the patterns in the X-rays.

After each convolution, I used MaxPooling to shrink the data size and focus on the most important features.

I also included a Dropout layer (0.5) before the final output. This was a key step for me because it forces the model to not rely too heavily on any single pixel pattern, making it more "honest" during testing.

Settings: Since there are only two classes (Pneumonia vs. Normal), I used Binary Cross-Entropy for the loss and the Adam optimizer to keep the training efficient.

3. What I Found
Training results: I ran the training for 10 epochs. I noticed that the accuracy went up steadily, and the validation curve followed the training curve pretty well. This told me the model was actually learning and not just memorizing.

Final Accuracy: When I tested the model on the final "Test" folder (data the model had never seen before), I got an accuracy of 88.94%.

Conclusion: Getting nearly 89% accuracy is a solid result for this type of medical data. It shows that the CNN is successfully picking up on the lung opacities that indicate pneumonia.