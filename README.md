## Next Video Frame Prediction

![image](https://github.com/riddhiman-ghatak/next_video_frame_prediction/assets/109431506/cea9b6bb-e9da-4b51-a3db-702f85009389)



<!-- ABOUT THE PROJECT -->

## About The Project

Video Frame Prediction is the task of predicting future frames given a set of past frames. Despite the fact that humans can easily and effortlessly solve the future frame prediction problem, it is extremely challenging for a machine. Complexities such as occlusions, camera movement, lighting conditions, or clutter make this task difficult for a machine. Predicting the next frames requires an accurate learning of the representation of the input frame sequence or the video. This task is of high interest as it caters to many applications such as autonomous navigation and self-driving. We present a novel Adversarial Spatio-Temporal Convolutional LSTM architecture to predict the future frames of the Moving MNIST Dataset. We evaluate the model on long-term future frame prediction and its performance of the model on out-of-domain inputs by providing sequences on which the model was not trained.



### Built With
This project was built with 

* python v3.8.5
* PyTorch v1.7
* The environment used for developing this project is available at [environment.yml](environment.yml).






## Model overview

The architecture of the model is shown below. The frame predictor model takes in the first ten frames as input and predicts the future ten frames. The
discriminator model tries to classify between the true future frames and predicted future frames. For the first ten time instances, we use the ground truth past frames as input, where as for the future time instances, we use the past predicted frames as input.

![image](https://github.com/riddhiman-ghatak/next_video_frame_prediction/assets/109431506/b6b14641-a005-4153-b3fa-ddf5368738b8)





<!-- RESULTS -->

## Results



We evaluate the performance of the model for long-term predictions to reveal its generalization capabilities. We provide the first 20 frames as input and let the model predict for the next 100 frames. 

Ground truth frames (1-10):

![image](https://github.com/riddhiman-ghatak/next_video_frame_prediction/assets/109431506/2a9c1528-7a3f-4548-888c-65b39ff2fb59)


Predicted frames (2-101):

![image](https://github.com/riddhiman-ghatak/next_video_frame_prediction/assets/109431506/2ea67825-95a4-4d71-9cc6-c050b09ee9f4)





We evaluate the performance of the model on out-of-domain inputs which the model has not seen during the training. We provide a frame sequence with one moving digit as input and observe the outputs from the model.

Ground truth frames (1-10):

![image](https://github.com/riddhiman-ghatak/next_video_frame_prediction/assets/109431506/3760ac9a-0c0d-4434-8d01-033612b4e377)



Predicted frames (2-41):

![image](https://github.com/riddhiman-ghatak/next_video_frame_prediction/assets/109431506/6e0f4076-8737-4300-a00e-2a0be74e2e12)





<!-- LICENSE -->

## License

Distributed under the MIT License. See `LICENSE` for more information.



