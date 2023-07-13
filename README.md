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

![image](https://github.com/riddhiman-ghatak/next_video_rame_prediction/assets/109431506/918908d4-db3c-4ff5-b456-53c67a46ac32)




<!-- RESULTS -->

## Results

Detailed results and inferences are available in report [here](./docs/report.pdf).

We evaluate the performance of the model for long-term predictions to reveal its generalization capabilities. We provide the first 20 frames as input and let the model predict for the next 100 frames. 

Ground truth frames (1-10):

![image](https://github.com/riddhiman-ghatak/next_video_rame_prediction/assets/109431506/21fa21b0-8715-4c6e-b4c2-149f763d0a80)

Predicted frames (2-101):

![image](https://github.com/riddhiman-ghatak/next_video_rame_prediction/assets/109431506/94452476-8c1e-471a-a74b-1d4966c70c2a)




We evaluate the performance of the model on out-of-domain inputs which the model has not seen during the training. We provide a frame sequence with one moving digit as input and observe the outputs from the model.

Ground truth frames (1-10):

![image](https://github.com/riddhiman-ghatak/next_video_rame_prediction/assets/109431506/48d30b8a-106c-448a-ad82-d5ae388e3b88)


Predicted frames (2-41):

![image](https://github.com/riddhiman-ghatak/next_video_rame_prediction/assets/109431506/c5eacf1d-fbb1-4fc5-b4cd-63960feca225)




<!-- LICENSE -->

## License

Distributed under the MIT License. See `LICENSE` for more information.



