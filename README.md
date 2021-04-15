![image](https://user-images.githubusercontent.com/56825699/114810188-212f9880-9dde-11eb-8fac-50dd0914c719.png)
# Noisy-Student_sample
This is simple implement of Noisy Student(https://arxiv.org/pdf/1911.04252.pdf) on HW3 of NTU-ML-2021-spring set up by prof.李宏毅 (Hung-yi Lee).The dataset is food-11 by removing part of label on training data.There are 11 class, 3,080 labeled training data, 6,786 unlabeled training data.

## Data Sample
![image](https://user-images.githubusercontent.com/56825699/114810034-ddd52a00-9ddd-11eb-978b-b14e0bb55283.png)


## Procedure
Follow the procedure of Noisy Student. First train a teacher model with labeled data -> generate pseudo-label on unlabeled training data by teacher model -> filter the unlabeled data by confidence -> balance the number of data for each class -> combine labeled data and pseudo-labeled data -> train a new student model on new dataset -> make student model as teacher model and repeat the procedure.
