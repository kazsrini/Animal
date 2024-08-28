# Animal

Purpose:
Classify species of animals based on pictures. Can automatically help identify animals in the wild taken by wildlife conservatories. Can lead to discoveries of potential new habitat as well as new unseen species of animals within the same class.

Method:
Train images of animals from six different species with thousands of labeled pictures in a VGG16 transfer learning model using Convulational Neural Network.

Dataset:
Data came from Animals-10 dataset in kaggle. Only chose six of the available species due to computer processing limitations, as well as fixed time window to run experiment.

All process and methods can be found in the Final Notebook
Final Model:
This is the final model that yielded the highest accuracy:

![image](https://github.com/user-attachments/assets/88b49dc9-efdd-46c3-96c3-722fbc4050a7)

![image](https://github.com/user-attachments/assets/f42ec173-ecd3-4393-bd20-7cefe31d5a3b)

![image](https://github.com/user-attachments/assets/2e9fa07c-28cd-4180-a6c2-b0e9d0afb654)


Our classification metrics shows that our model has relatively high precision accuracy for all our image categories, letting us know that this is a valid model:

![image](https://github.com/user-attachments/assets/455480b7-d95c-4301-b6b7-734d8d8c68a9)

In addition, our confusion matrix also shows how well the model predicted for each class and how often it was wrong:

![image](https://github.com/user-attachments/assets/b56b1826-d69e-424c-b043-4370d3cd517c)

This is mainly due to class imbalance. Some categories had more pictures then others.

Test a picture:
![image](https://github.com/user-attachments/assets/e4c8f828-9e5f-4872-9262-f1d91098890e)


Issues:
The biggest issue was class imbalance. Since there were uneven numbers of pictures for each samples, this led the algorithm to train better on some categories versus the others. Second issues is we did not add any more than basic distortions in our picture. But this led to better training as I later tested it with distorted pictures, and it was still able to correctly guess the picture. It was of a brown recluse spider with added noise.

Conclision:
This model can excellently guess a picture of an animal if the shape of the animal is in the training method. To train it in additional animals, simply feed it labeled images (1000 at least for training and 300+ for validation). Also, just for fun, you can also give the machine a picture of a pokemon like Rapidash and it will guess it is a horse.
