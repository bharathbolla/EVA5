# EVA5
EVA5 Phase=1 Deep Learning Course by The School of AI


## First Model

## Target:
   ### 1. Get the basic structure right - All cells must run corretly for a DNN task.
   ### 2. Add ReLU and BatchNorm in every convolution layer except at last before output layer
   ### 3. Make the model lighter - With less than 10k parameter
   ### 4. Add maxpooling at RF = 5 (by looking at the image)
   ### 5. Add Gobal average pooling

## Result:
   ### 1. Parameters: 7,600
   ### 2. Best train accuracy: 99.13
   ### 3. Best test accuracy: 99.07(13th epoch)

## Analysis:
   ### 1. The model is good and light
   ### 2. At 19th epoch train accuracy: 99.33 and test accuracy: 99.04 (we see overfitting)
   ### 3. Need to use Regularization

## Second Model

## Target:
  ### 1.Add Regularization-Dropout.
  ### 2.Add Dropout to each layer.

## Result:
   ### 1.Parameter:7,600
   ### 2.Best train accuracy:98.34
   ### 3.best test accuracy:99.02(14th epoch)

## Analysis:
   ### 1.The model is not over-fitting.
   ### 2.The model is under fitting because we using droupout to every layer and making model to train hard.
   ### 3.Add a layer after Gobal average pooling. Adding dense layer after GAP

