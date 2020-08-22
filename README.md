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
   
## Third Model
## Target:
    ## 1.Increase capacity of model.
    ## 2.Add a layer after Gobal average pooling.Adding dense layer after GAP

## Result:
    ## 1.Parameters:9,660
    ## 2.Best train accuracy:98.84
    ## 3.Best test accuracy:99.39(13th epoch)

## Analysis:
   ## 1:The model is not over fitting.
   ## 2.At (18th epoch) train accuracy:98.92 and test accuracy:99.46 .
   ## 3.But we are not getting 99.40+ below 15th epoch.
   ## 4.Try LR OPtimizers and schedulers

## Fourth Model
## Target:
   ### 1. Increase the capacity of the model

## Result:
   ### 1.Parameters:9,980
   ##3 2.Best train accuracy:98.89
   ### 3.Best test accuracy:99.37(15th epoch)


## Fifth Model
## Analysis:
   ### 1.We got test accuracy: 99.47 and 99.45 (17th and 19th epoch).
   ### 2.The model is not over fitting .
   ### 3.By seeing images all numbers are not in same shape.So, add rotation
 ## Target:
   ### 1.Add rotation 
   ### 2. Add Onestep Cycle LR policy

## Result:
  ### 1:Parameters:9,980
  ### 2.Best train accuracy:98.67
  ### 3.Best test accuracy:99.44(15th epoch)

## Analysis:
   ### 1:The model is working.
   ### 2:we can see 99.4+ being acheived in the last four epochs.
   ### 3:The test accuracy increased because of RandomRotation 
   ### 4. The consistency and 99.4 was acheived so early because of one step cycle LR
 
 
 ## Model
 ----------------------------------------------------------------
        Layer (type)               Output Shape         Param #
================================================================
            Conv2d-1           [-1, 16, 26, 26]             144
              ReLU-2           [-1, 16, 26, 26]               0
       BatchNorm2d-3           [-1, 16, 26, 26]              32
         Dropout2d-4           [-1, 16, 26, 26]               0
            Conv2d-5           [-1, 32, 24, 24]           4,608
              ReLU-6           [-1, 32, 24, 24]               0
       BatchNorm2d-7           [-1, 32, 24, 24]              64
         Dropout2d-8           [-1, 32, 24, 24]               0
            Conv2d-9            [-1, 8, 24, 24]             256
        MaxPool2d-10            [-1, 8, 12, 12]               0
           Conv2d-11           [-1, 14, 10, 10]           1,008
             ReLU-12           [-1, 14, 10, 10]               0
      BatchNorm2d-13           [-1, 14, 10, 10]              28
        Dropout2d-14           [-1, 14, 10, 10]               0
           Conv2d-15             [-1, 16, 8, 8]           2,016
             ReLU-16             [-1, 16, 8, 8]               0
      BatchNorm2d-17             [-1, 16, 8, 8]              32
        Dropout2d-18             [-1, 16, 8, 8]               0
           Conv2d-19             [-1, 10, 8, 8]             160
           Conv2d-20             [-1, 16, 6, 6]           1,440
             ReLU-21             [-1, 16, 6, 6]               0
      BatchNorm2d-22             [-1, 16, 6, 6]              32
        Dropout2d-23             [-1, 16, 6, 6]               0
        AvgPool2d-24             [-1, 16, 1, 1]               0
           Conv2d-25             [-1, 10, 1, 1]             160
================================================================
Total params: 9,980
Trainable params: 9,980
Non-trainable params: 0
----------------------------------------------------
 ## Logs
  0%|          | 0/469 [00:00<?, ?it/s]
Test set: Average loss: 0.0270, Accuracy: 9911/10000 (99.11%)

EPOCH: 6
Loss=0.023547517135739326 Batch_id=468 Accuracy=98.41: 100%|██████████| 469/469 [00:13<00:00, 33.52it/s]Epoch: 6 LR: [0.0866309437466121]

  0%|          | 0/469 [00:00<?, ?it/s]
Test set: Average loss: 0.0266, Accuracy: 9916/10000 (99.16%)

EPOCH: 7
Loss=0.007044315803796053 Batch_id=468 Accuracy=98.47: 100%|██████████| 469/469 [00:14<00:00, 33.39it/s]Epoch: 7 LR: [0.0749724709105188]

  0%|          | 0/469 [00:00<?, ?it/s]
Test set: Average loss: 0.0257, Accuracy: 9922/10000 (99.22%)

EPOCH: 8
Loss=0.04992355406284332 Batch_id=468 Accuracy=98.67: 100%|██████████| 469/469 [00:13<00:00, 33.55it/s]Epoch: 8 LR: [0.061095102215020056]

  0%|          | 0/469 [00:00<?, ?it/s]
Test set: Average loss: 0.0231, Accuracy: 9920/10000 (99.20%)

EPOCH: 9
Loss=0.006587113719433546 Batch_id=468 Accuracy=98.73: 100%|██████████| 469/469 [00:14<00:00, 33.09it/s]Epoch: 9 LR: [0.046231902768540376]

  0%|          | 0/469 [00:00<?, ?it/s]
Test set: Average loss: 0.0258, Accuracy: 9916/10000 (99.16%)

EPOCH: 10
Loss=0.14703263342380524 Batch_id=468 Accuracy=98.76: 100%|██████████| 469/469 [00:14<00:00, 33.40it/s]Epoch: 10 LR: [0.031703533067975895]

  0%|          | 0/469 [00:00<?, ?it/s]
Test set: Average loss: 0.0236, Accuracy: 9931/10000 (99.31%)

EPOCH: 11
Loss=0.05253337696194649 Batch_id=468 Accuracy=98.95: 100%|██████████| 469/469 [00:14<00:00, 33.46it/s]Epoch: 11 LR: [0.018800902517922092]

  0%|          | 0/469 [00:00<?, ?it/s]
Test set: Average loss: 0.0192, Accuracy: 9941/10000 (99.41%)

EPOCH: 12
Loss=0.05755201354622841 Batch_id=468 Accuracy=99.00: 100%|██████████| 469/469 [00:14<00:00, 33.50it/s]Epoch: 12 LR: [0.008670466465012771]

  0%|          | 0/469 [00:00<?, ?it/s]
Test set: Average loss: 0.0196, Accuracy: 9940/10000 (99.40%)

EPOCH: 13
Loss=0.0050410921685397625 Batch_id=468 Accuracy=99.03: 100%|██████████| 469/469 [00:13<00:00, 33.62it/s]Epoch: 13 LR: [0.0022123586092353013]

  0%|          | 0/469 [00:00<?, ?it/s]
Test set: Average loss: 0.0190, Accuracy: 9940/10000 (99.40%)

EPOCH: 14
Loss=0.0388953797519207 Batch_id=468 Accuracy=99.07: 100%|██████████| 469/469 [00:14<00:00, 33.48it/s]Epoch: 14 LR: [4.101745150496986e-07]


Test set: Average loss: 0.0183, Accuracy: 9944/10000 (99.44%)


