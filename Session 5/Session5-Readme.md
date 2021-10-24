In this project, the Goal is to achieve 99.4% accuracy with less than 10k Parameter. Lets build the network sequentially and see if can achieve our target.

1st Attempt

    1. Get the setup right
    2. have the basic skeleton
    3. Results:
        a. Parameters: 6.3M
        b. Best Train Accuracy: 90.12
        c. Best Test Accuracy: 89.79
    4. Analysis:
        a. Model is heavy for such data
        b. Model is overfitting

    Code is available at : https://colab.research.google.com/drive/1Pn8260YzfE-yj4CSPsa_HAlFXJD7_OfC#scrollTo=aO-7t1Y7-hV4

2nd Attempt

    1. Make the Model lighter, if possible, less than 20K parameters
    2. Results:
        a. Parameters: 12, 690K
        b. Best Train Accuracy: 99.14
        c. Best Test Accuracy: 98.66
    3. Analysis:
        a. We see some under fitting in the initial epoch, test accuracy is greater than train accuracy
        b. Train Accuracy is better, let’s try to push more on the next attempt

    Code is available at : https://colab.research.google.com/drive/15KKcMiaMcziPBe2_Lk0lLbPs1B7kqHwG

3rd Attempt

    1. Lets try to increase Train accuracy and let’s add Batch Normalization for each block, never add Batch Normalization to the last layer
    2. If not able to achieve the target, let’s add Regularization (Dropout) to our model
    3. Results:
        a. Parameters: 10,490
        b. Best Train Accuracy: 99
        c. Best Test Accuracy: 99.28
    4. Analysis:
        a. Initially without drop, we were able to achieve 99.4+ train accuracy consistently we even reached 99.7
        b. But still there is some overfitting can be seen, so adding 0.1 dropout to our model

    Code is available at : https://colab.research.google.com/drive/1tb1QXQr5AFemc_STRwaivJJIBYGyW6p0

4th Attempt:

    1. Must it 99.4 for minimum 3 times under 15 epochs
    2. Will add Image augmentation if not able to achieve 99.4 accuracy
    3. Results:
        a. Parameters: 9032K
        b. Best Train Accuracy: 99.45
        c. Best Test Accuracy: 98.9
    4. Analysis:
        a. Made our model little bit lighter
        b. Increasing learning rate helped model to learn faster, so able to achieve

    Code is available at : https://colab.research.google.com/drive/1Pnwcmz7YS_2rvZSc_QmlLekkba-lARac#scrollTo=aE5Le6FYHhc8
