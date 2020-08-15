# EVA5
## Session_4 Assignment

### Acheived final accuracy of 99.42 (13th epoch). Used Batchnorm, maxpool and  dropout. Experimented with dropout. Dropout with 0.05 is better than dropout with 0.10.
### Highest accuracy of 99.48 at 17th epoch
### Total number of parameters 12,400
### Total Seven conv2d layers.


### Model Parameters Summary

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
           Conv2d-11           [-1, 16, 10, 10]           1,152
             ReLU-12           [-1, 16, 10, 10]               0
      BatchNorm2d-13           [-1, 16, 10, 10]              32
        Dropout2d-14           [-1, 16, 10, 10]               0
           Conv2d-15             [-1, 16, 8, 8]           2,304
             ReLU-16             [-1, 16, 8, 8]               0
      BatchNorm2d-17             [-1, 16, 8, 8]              32
        Dropout2d-18             [-1, 16, 8, 8]               0
           Conv2d-19             [-1, 16, 8, 8]           2,304
             ReLU-20             [-1, 16, 8, 8]               0
      BatchNorm2d-21             [-1, 16, 8, 8]              32
        Dropout2d-22             [-1, 16, 8, 8]               0
           Conv2d-23             [-1, 10, 6, 6]           1,440
        AvgPool2d-24             [-1, 10, 1, 1]               0
================================================================
Total params: 12,400
Trainable params: 12,400
Non-trainable params: 0


### Logs

0%|          | 0/469 [00:00<?, ?it/s]/usr/local/lib/python3.6/dist-packages/ipykernel_launcher.py:61: UserWarning: Implicit dimension choice for log_softmax has been deprecated. Change the call to include dim=X as an argument.
loss=0.09364736080169678 batch_id=468: 100%|██████████| 469/469 [00:12<00:00, 36.47it/s]
  0%|          | 0/469 [00:00<?, ?it/s]
Test set: Average loss: 0.0646, Accuracy: 9817/10000 (98.17%)

loss=0.08194563537836075 batch_id=468: 100%|██████████| 469/469 [00:12<00:00, 37.48it/s]
  0%|          | 0/469 [00:00<?, ?it/s]
Test set: Average loss: 0.0390, Accuracy: 9890/10000 (98.90%)

loss=0.05425289645791054 batch_id=468: 100%|██████████| 469/469 [00:12<00:00, 36.44it/s]
  0%|          | 0/469 [00:00<?, ?it/s]
Test set: Average loss: 0.0325, Accuracy: 9891/10000 (98.91%)

loss=0.05338434875011444 batch_id=468: 100%|██████████| 469/469 [00:13<00:00, 34.73it/s]
  0%|          | 0/469 [00:00<?, ?it/s]
Test set: Average loss: 0.0325, Accuracy: 9899/10000 (98.99%)

loss=0.17614750564098358 batch_id=468: 100%|██████████| 469/469 [00:13<00:00, 35.40it/s]
  0%|          | 0/469 [00:00<?, ?it/s]
Test set: Average loss: 0.0278, Accuracy: 9916/10000 (99.16%)

loss=0.02227477915585041 batch_id=468: 100%|██████████| 469/469 [00:13<00:00, 33.88it/s]
  0%|          | 0/469 [00:00<?, ?it/s]
Test set: Average loss: 0.0242, Accuracy: 9931/10000 (99.31%)

loss=0.10178112983703613 batch_id=468: 100%|██████████| 469/469 [00:13<00:00, 35.03it/s]
  0%|          | 0/469 [00:00<?, ?it/s]
Test set: Average loss: 0.0215, Accuracy: 9928/10000 (99.28%)

loss=0.008401498198509216 batch_id=468: 100%|██████████| 469/469 [00:12<00:00, 36.77it/s]
  0%|          | 0/469 [00:00<?, ?it/s]
Test set: Average loss: 0.0245, Accuracy: 9922/10000 (99.22%)

loss=0.038491468876600266 batch_id=468: 100%|██████████| 469/469 [00:12<00:00, 36.77it/s]
  0%|          | 0/469 [00:00<?, ?it/s]
Test set: Average loss: 0.0205, Accuracy: 9933/10000 (99.33%)

loss=0.04686379432678223 batch_id=468: 100%|██████████| 469/469 [00:12<00:00, 37.39it/s]
  0%|          | 0/469 [00:00<?, ?it/s]
Test set: Average loss: 0.0219, Accuracy: 9931/10000 (99.31%)

loss=0.031477782875299454 batch_id=468: 100%|██████████| 469/469 [00:13<00:00, 34.99it/s]
  0%|          | 0/469 [00:00<?, ?it/s]
Test set: Average loss: 0.0221, Accuracy: 9935/10000 (99.35%)

loss=0.01987368054687977 batch_id=468: 100%|██████████| 469/469 [00:13<00:00, 34.29it/s]
  0%|          | 0/469 [00:00<?, ?it/s]
Test set: Average loss: 0.0196, Accuracy: 9942/10000 (99.42%)

loss=0.03662765398621559 batch_id=468: 100%|██████████| 469/469 [00:13<00:00, 34.41it/s]
  0%|          | 0/469 [00:00<?, ?it/s]
Test set: Average loss: 0.0188, Accuracy: 9941/10000 (99.41%)

loss=0.029962792992591858 batch_id=468: 100%|██████████| 469/469 [00:13<00:00, 34.16it/s]
  0%|          | 0/469 [00:00<?, ?it/s]
Test set: Average loss: 0.0195, Accuracy: 9935/10000 (99.35%)

loss=0.06444106996059418 batch_id=468: 100%|██████████| 469/469 [00:13<00:00, 33.80it/s]
  0%|          | 0/469 [00:00<?, ?it/s]
Test set: Average loss: 0.0192, Accuracy: 9939/10000 (99.39%)

loss=0.019809221848845482 batch_id=468: 100%|██████████| 469/469 [00:13<00:00, 34.15it/s]
  0%|          | 0/469 [00:00<?, ?it/s]
Test set: Average loss: 0.0178, Accuracy: 9948/10000 (99.48%)

loss=0.04336307570338249 batch_id=468: 100%|██████████| 469/469 [00:13<00:00, 34.53it/s]
  0%|          | 0/469 [00:00<?, ?it/s]
Test set: Average loss: 0.0180, Accuracy: 9946/10000 (99.46%)

loss=0.06512411683797836 batch_id=468: 100%|██████████| 469/469 [00:13<00:00, 34.65it/s]
  0%|          | 0/469 [00:00<?, ?it/s]
Test set: Average loss: 0.0168, Accuracy: 9944/10000 (99.44%)

loss=0.012609169818460941 batch_id=468: 100%|██████████| 469/469 [00:13<00:00, 34.32it/s]

Test set: Average loss: 0.0199, Accuracy: 9934/10000 (99.34%)
