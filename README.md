
# DeepWeeds Classification Project

## Overview

This project focuses on the classification of weed species using the DeepWeeds dataset, which contains images of eight different weed species native to Australia. The main objective is to develop a deep learning model capable of accurately identifying these weed species from images.

## Dataset: DeepWeeds

The DeepWeeds dataset consists of 17,509 images capturing eight different weed species native to Australia in situ with neighboring flora. These species are common to pastoral grasslands in Queensland, Australia. The images were collected from various locations across Queensland, including Black River, Charters Towers, Cluden, Douglas, Hervey Range, Kelso, McKinlay, and Paluma.

- **Total Images**: 17,509
- **Number of Classes**: 8 weed species
- **Image Size**: 256x256 pixels
- **Data Source**: [DeepWeeds GitHub Repository](https://github.com/AlexOlsen/DeepWeeds)

### Dataset Split

The dataset was divided into training and testing sets:
- **Training Set**: 14,007 images (80%)
- **Testing Set**: 3,502 images (20%)

### Example Images from the Dataset

![Example Image 1](https://camo.githubusercontent.com/17520c5c3dc2dfc7537862d604e084cbeacd8d9066c0ff08a58104c455ae3cb9/68747470733a2f2f692e696d6775722e636f6d2f3265306f77386c2e706e67)

![Example Image 2](https://camo.githubusercontent.com/5c4f84751644ecc545bf5dde4717e69083569f0efff777ebc84fd4501d90317f/68747470733a2f2f692e696d6775722e636f6d2f73636d4a6353332e6a7067)

## Model and Training

The model used in this project is a convolutional neural network (CNN) designed to handle image classification tasks. The following steps were applied to train the model:

1. **Data Augmentation**: To improve the model's robustness and prevent overfitting, various data augmentation techniques were used, including random rotations, flipping, and zooming of the images.
2. **Oversampling**: To balance the training dataset, oversampling was applied using the `RandomOverSampler` from the `imblearn` library. This technique was used to ensure that all classes are equally represented in the training set, which helps improve the model's accuracy across all classes.
3. **Training**: The model was trained using the augmented and oversampled dataset with a specific training configuration, optimizing for accuracy.

## Performance

The model achieved a test accuracy of **86.44%**, demonstrating its effectiveness in classifying the different weed species in the dataset.

## Conclusion

This project successfully applied deep learning techniques to classify weed species from images, using the DeepWeeds dataset. The achieved accuracy indicates that such models can be valuable tools for automating weed identification, which could benefit agricultural management practices.

## Citation

If you use the DeepWeeds dataset in your research, please cite the following paper:

```bibtex
@article{DeepWeeds2019,
  author = {Alex Olsen and
    Dmitry A. Konovalov and
    Bronson Philippa and
    Peter Ridd and
    Jake C. Wood and
    Jamie Johns and
    Wesley Banks and
    Benjamin Girgenti and
    Owen Kenny and
    James Whinney and
    Brendan Calvert and
    Mostafa {Rahimi Azghadi} and
    Ronald D. White},
  title = { {DeepWeeds: A Multiclass Weed Species Image Dataset for Deep Learning} },
  journal = {Scientific Reports},
  year = 2019,
  number = 2058,
  month = 2,
  volume = 9,
  issue = 1,
  day = 14,
  url = "https://doi.org/10.1038/s41598-018-38343-3",
  doi = "10.1038/s41598-018-38343-3"
}
```
