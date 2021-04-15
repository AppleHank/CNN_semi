![image](https://user-images.githubusercontent.com/56825699/114810255-42908480-9dde-11eb-8091-700dbb759f44.png)
# Noisy-Student_sample
This is simple implement of Noisy Student(https://arxiv.org/pdf/1911.04252.pdf) on HW3 of NTU-ML-2021-spring set up by prof.李宏毅 (Hung-yi Lee).The dataset is food-11 by removing part of label on training data.There are 11 class, 3,080 labeled training data, 6,786 unlabeled training data.

## Data Sample
![image](https://user-images.githubusercontent.com/56825699/114810034-ddd52a00-9ddd-11eb-978b-b14e0bb55283.png)


## Procedure
Follow the procedure of Noisy Student. First train a teacher model with labeled data -> use teacher model to generate pseudo-label on unlabeled data -> filter the pseudo-labeled data by confidence -> balance the number of data for each class -> combine labeled data and pseudo-labeled data -> train a student model on new dataset -> make student model as teacher model and repeat the procedure.  
Note that in the original paper, they perform augmentation in both data and model, In data augmentation, RandAugment is used. In model augmentation, dropout and stochastic depth is used. However, this sample did'nt use stochastic depth because the dataset is too small to build a deep model.
