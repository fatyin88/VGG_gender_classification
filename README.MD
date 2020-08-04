# VGG Gender and Age Classification

Using conv network to classify gender and age.

In paper [Age and Gender Classification using Convolutional Neural Networks](https://www.openu.ac.il/home/hassner/projects/cnn_agegender/CNN_AgeGenderEstimation.pdf), author come up a model of conv netowrk to estimate gender and age.

I reproduce their work in tensorflow and make some improvment.

Dataset: [Adience Benchmark](https://www.openu.ac.il/home/hassner/Adience/data.html#agegender). For this project, we’ll use the Adience dataset. This dataset serves as a benchmark for face photos and is inclusive of various real-world imaging conditions like noise, lighting, pose, and appearance. The images have been collected from Flickr albums and distributed under the Creative Commons (CC) license. It has a total of 26,580 photos of 2,284 subjects in eight age ranges (as mentioned above) and is about 1GB in size. The models we will use have been trained on this dataset.


```
origin from: https://github.com/zealerww/gender_age_classification

```

## Experiments

1. reproduce their work(called model_origin later)
2. using other networks, such as inception-like, resnet-like
3. using bathnormalization, change activation function
4. using pre-trained VGG face network and fine tune fully connected layers

model_origin get **85.9%** accuracy in gender and **49.5%** in age.

Replacing the model_origin with inception-like/resnet-like netowork don't get significant improvement. Using selu as the activation function can get **2% improvement** in gender estimation.

VGG face network is a network for face recogniton, I use it as a face feature extractor. It is a good base model. Using pre-trained conv layers of VGG face network and fine-tuning fully connected layers gets **91%** accuracy in gender and **55%** in age.

You get get pre-trained VGG face network weight [here](https://drive.google.com/file/d/1swNHi9XMh0GJs8eBEhw2xjCAN07JjfT9/view?usp=sharing)

## Others

Multi-cropping can get a little improvement but consuming more time.
