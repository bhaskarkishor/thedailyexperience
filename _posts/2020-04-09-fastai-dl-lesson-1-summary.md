---
layout: post
title: Image Classification by fast.ai, lesson 1
image: images/fastai.png
tags: [deep learning]
---

Deep learning course on [fast ai](fast.ai) is one of the
best MOOCs that I feel actually gets you going. It has implemented
the top down approach of learning machine learning correctly.
In my case, Initially like many I started with basics first to
learn Data Science but soon I relaised this method is not
good enough. It doesn't arouse curiosity, which is necessary
for moving forward in any domain.

So here, I am just going to mention a quick summary of first lesson
of deep learning MOOC. It deals with *Image Classification*.

#### what if I don't have a high performing gpu and loads of dat?
Here, its a valid question that might stop many from applying
deep learning because as everyone knows a deep learning model
requires large amount of data. But actually it is half truth.
You don't always need large amount of data for training 
a deep learning neural net. You can leverage the power of
pretrained models to train your model. The trick is not to start from scratch. Use a model which
already knows about images. This is called *Transfer Learning*.

As for a gpu, there are some free and paid alternative availbale
in the cloud to run a decent gpu for coursework. Such as
kaggle and colab offers a free gpu with limited hours. 
Amazon aws offers gpu at cheap price and for more go to
Fast.ai docs page.

#### Classification model using a CNN model with pretrained weights
Later, Jeremy discusses about some pretrained models available for image
classification. Resnet35 and Resnet50 are two models with
pretrained weights for images.

In Resnet35, the number 35 represents number of layers included
in neural net. Resnet35 and Resnet50 are known to perform
quite well in comparision to other layers.
 
##### But isn't it true that more number of layers simply improves 
the quality of model, then why this preference of 35 and 50? 

To answer this question we need to look into how the various layered
structure of neural nets work. It was explained that different layers
identified different patterns in images. Later lower level layers are
combined to form complex layer. So while training the models
unfreezing all the layers would cause the model to oerform worse.
At this stage, just train model with your images to get your model.

Jeremy shows an example of a model which was trained over less than
20 images to differentiate between baseball and cricket. Surprisingly,
it turms out quite well. The model work pretty correctly.


All in all, deep learning is not a far from your reach. You just need to
run the code to get the hang of it.

