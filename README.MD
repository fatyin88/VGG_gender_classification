# VGG Gender Classification (MM Assignment)

Using conv network to classify gender. (My project only focus on Gender Classification) 

In paper [Age and Gender Classification using Convolutional Neural Networks](https://www.openu.ac.il/home/hassner/projects/cnn_agegender/CNN_AgeGenderEstimation.pdf), author come up a model of conv network to estimate gender and age.

Knowing that using pre-trained VGG face network and fine tune fully connected layers can obtain a better performance than the CNN model mentioned in the paper above, I would like to do an experiment to see if it can really outperform the original model.  

Dataset: [Adience Benchmark](https://www.openu.ac.il/home/hassner/Adience/data.html#agegender). For this project, we’ll use the Adience dataset. This dataset serves as a benchmark for face photos and is inclusive of various real-world imaging conditions like noise, lighting, pose, and appearance. The images have been collected from Flickr albums and distributed under the Creative Commons (CC) license. It has a total of 26,580 photos of 2,284 subjects in eight age ranges (as mentioned above) and is about 1GB in size. The models we will use have been trained on this dataset.


```
origin from: https://github.com/zealerww/gender_age_classification

```

## Experiments

Using pre-trained VGG face network and fine tune fully connected layers

CNN model get **85.9%** accuracy in gender.

VGG face network is a network for face recogniton, I use it as a face feature extractor. It is a good base model. Using pre-trained conv layers of VGG face network and fine-tuning fully connected layers gets **91%** accuracy in gender.

You get get pre-trained VGG face network weight [here](https://drive.google.com/file/d/1swNHi9XMh0GJs8eBEhw2xjCAN07JjfT9/view?usp=sharing)

## Others

Multi-cropping can get a little improvement but consuming more time.
