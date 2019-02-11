# Animal Image Classification using CNN

For our module 4 project, my partner [Vicente](https://github.com/vaeb80) and I wanted to create an image classifier using deep learning. 

### Purpose:

Classify species of animals based on pictures. Can automatically help identify animals in the wild taken by wildlife conservatories. Can lead to discoveries of potential new habitat as well as new unseen species of animals within the same class.

### Method:

Train images of animals from six different species with thousands of labeled pictures in a VGG16 transfer learning model using Convulational Neural Network.

### Dataset:

Data came from [Animals-10](https://www.kaggle.com/alessiocorrado99/animals10) dataset in kaggle. Only chose six of the available species due to computer processing limitations, as well as fixed time window to run experiment.

#### All process and methods can be found in the [Final Notebook](https://github.com/imamun93/animal-image-classifications/blob/master/final_notebook.ipynb)

### Final Model:

This is the final model that yielded the highest accuracy: 

![image](https://user-images.githubusercontent.com/41834786/52592607-d5a38d80-2e14-11e9-8a6b-b079c9c991f3.png)


![image](https://user-images.githubusercontent.com/41834786/52592643-ec49e480-2e14-11e9-993e-f58a888884ae.png)

![image](https://user-images.githubusercontent.com/41834786/52592685-0aafe000-2e15-11e9-8e89-b530951c6b6e.png)

Our classification metrics shows that our model has relatively high precision accuracy for all our image categories, letting us know that this is a valid model:

<img width="729" alt="screen shot 2019-02-11 at 4 01 27 pm" src="https://user-images.githubusercontent.com/41834786/52593175-51520a00-2e16-11e9-82b4-31c056cbc834.png">

In addition, our confusion matrix also shows how well the model predicted for each class and how often it was wrong:

![image](https://user-images.githubusercontent.com/41834786/52593252-7b0b3100-2e16-11e9-98ca-518fa96d0d9f.png)

This is mainly due to class imbalance. Some categories had more pictures then others.

## Test a picture:

![image](https://user-images.githubusercontent.com/41834786/52593571-451a7c80-2e17-11e9-8d8e-44eb79d7e842.png)

### Issues:

The biggest issue was class imbalance. Since there were uneven numbers of pictures for each samples, this led the algorithm to train better on some categories versus the others. Second issues is we did not add any more than basic distortions in our picture. But this led to better training as I later tested it with distorted pictures, and it was still able to correctly guess the picture. It was of a brown recluse spider with added noise.

### Conclision:

This model can excellently guess a picture of an animal if the shape of the animal is in the training method. To train it in additional animals, simply feed it labeled images (1000 at least for training and 300+ for validation). Also, just for fun, you can also give the machine a picture of a pokemon like Rapidash and it will guess it is a horse.
