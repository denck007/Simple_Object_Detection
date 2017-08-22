# Simple_Object_Detection
Simple fully convolutional neural network for detecting and localizing objects. The model is based loosely on YOLO9000 [https://arxiv.org/abs/1612.08242], mostly the loss function resembles the YOLO loss function. 


To keep the model simple and quick to run, I am making images on the fly using MNIST. A black 64x64 background is created and random MNIST digits are placed randomly on the large image. The digits are randomly scaled  before being added onto the background. This approach seems to work pretty well for working though this project. The train time is ~72s/epoch (60000 large images) on a GTX750 with batchsize of 24. I have been running the model for 5 epochs in testing and it seems to have good localization and okay classification at that point.

The notebooks track progress through the project:
1) Convolutional_MNIST_Detection: Detection of 1 object
2) Convolutional_MNIST_Multipoint_Detection: Detection of 2 objects
3) Convolutional_MNIST_Multipoint_Detection_With_Confidence: Detection of upto 2 objects (random number of objects) 

