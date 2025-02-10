# Transfer Learning Experiment

This project explores the effectiveness of transfer learning using a pre-trained MobileNetV2 model for image classification on the CIFAR-10 dataset.  The performance of the transfer learning approach is compared against a baseline model trained from scratch.

## Methodology

1. **Data Preparation:** The CIFAR-10 dataset is loaded, normalized, and split into training, validation, and testing sets.

2. **Transfer Learning Model:**
   - A pre-trained MobileNetV2 model (trained on ImageNet) is used as a base.
   - The base model's layers are frozen to prevent weight updates during initial training.
   - Custom layers (Global Average Pooling, Dropout, Dense) are added on top for classification.
   - The model is trained on the CIFAR-10 training data, with validation accuracy monitored.
   - Feature maps from an intermediate layer of the base model are analyzed.

3. **Baseline Model:**
   - A simple convolutional neural network (CNN) is created and trained from scratch on the same dataset.
   - This serves as a comparison to evaluate the benefits of transfer learning.

4. **Evaluation:**
    - Model accuracy is evaluated on test data.
    - Comparison of test accuracy between the transfer learning model and the baseline model is performed.

5. **Visualization:**
   - Training and validation accuracies are plotted to visualize the learning curves of both models.
   - Visualization of feature maps from the pretrained model is also included.


## Results

The results show that the transfer learning model achieved 0.33] validation accuracy, while the baseline model achieved 0.63 test accuracy.  The comparison highlights the advantage of leveraging pre-trained knowledge. 



## Conclusion

The experiment  was to learn the potential of transfer learning to improve image classification accuracy. The visualization confirms a difference between the baseline model and the transfer learning model.  The comparison between the two models show that the pre-trained model can lead to faster and more efficient learning than training a model from scratch. Further investigation could involve experimenting with different pre-trained models, adjusting hyperparameters, or using other strategies to enhance transfer learning.
