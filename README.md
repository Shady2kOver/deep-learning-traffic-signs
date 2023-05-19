

## Background

The development of self-driving cars requires robust computer vision capabilities, including the ability to accurately recognize and classify road signs. 

As a first deep learning project, part of the CS50AI curriculum, we employ TensorFlow to construct a convolutional neural network that excels at identifying road signs based on provided images. We used the German Traffic Sign Recognition Benchmark (GTSRB) dataset, which has a range of labeled images featuring 43 distinct road sign categories.

We are using categorical classification, most people choose binary for their first project but this was part of the curriculum

## Details

 - The requirements (version inclusive unlike the original project , which made me encounter many many errors) are also in the repo
 - The dataset may or may not have been uploaded properly, it's all ppm files because thats what the german traffic sign recognition benchmark 

## Project Analysis
Summary of all different changes that were applied to my model during training process.

| Step | Observation | Inference | Action Taken |
|------|-------------|-----------|--------------|
| 1    | The model exhibited overfitting, with a training accuracy of 92.35% and a validation accuracy of 88.92% | The model was capturing the training data patterns well but struggled to generalize to unseen data | Introduced a dropout layer to regularize the model and reduce overfitting |
| 2    | After implementing dropout of 0.5, the model showed reduced overfitting with a training accuracy of 90.20% and a validation accuracy of 93.78% | The dropout layer effectively prevented overfitting by randomly dropping connections during training | Increased model complexity by adding more convolutional filters to capture finer details |
| 3    | While the model achieved good accuracy (training: 90.20%, validation: 93.78%), the training and validation loss continued to decrease at a similar rate | The model was performing well and had a good balance between underfitting and overfitting | Saved the trained model for future use |
| 4    | In the final few epochs, there was a slight indication of overfitting as the training accuracy remained high (93.74%) while the validation accuracy plateaued at 90.83% | The model was potentially memorizing the training data and not generalizing well to unseen examples | Increased dropout to 0.4 to further regularize the model and reduce overfitting, and exported the final model for future use |

## Conclusion
**Final**: The model achieved exceptional performance with a training accuracy of *95.04%* and a validation accuracy of *95.52%*  The model successfully learned the patterns in the training data and generalized well to unseen examples. The final model demonstrates the effectiveness of the chosen architecture and hyperparameters, and can be used for accurate categorical classification tasks. 

*File is saved as model.h5 in the same directory, the training dataset is also provided within*
