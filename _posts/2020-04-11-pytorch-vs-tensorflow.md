---
layout: post
title: Starting journey of deep learning - Pytorch vs Tensorflow ?
date: 2020-04-11
tags: [deep learning]
image: https://source.unsplash.com/gnyA8vd3Otc/1600*900
---

The deep learning domain in python environment has gained traction in last decade. That is beyond doubt and is constantly growing. And then comes
the list of popular libraries with it. Here, I am listiing two popular libraries and its differences which could be used for deep learning.
So let's get started.

#### Tensorflow
It is the most widely popular framework of choice among Deep Learning enthusiasts and industry developers. It is actively develpoed and maintained by
Google. Recently, they released an updated version, Tensorflow 2. The name itself attracts attention as all of us have experienced the capabilities of google's AI. It uses the underlying keras model
but more like it is built on it with adding features to it. 

Due to its popularity, it's easier to find tutorials and solution over stackexchage for some issue. However,
some believe that Tensorflow has higher learning curve than pyTorch and it is more suitable for production. Ease of deployment could easily
be understood from number of devices tensorflow supports ie. web, android, ios etc. TensorBoard is a great visualization tool available
int his envionment which has no inbuilt match in pytorch except for some ported implementations.

The graphs generated in tensorflow are static unlike pytorch whic could be a real bummer while working with RNNs. Tensorflow feels more like
a library than a framework because it gives you so much low level support. Its good for those who know what they are doing as it gives more 
control over the model. But writing more line of codes makes it susceptible to bugs also.

#### Pytorch
It can be regarded as one of the popular framewworks in deep learning domain, as it has also gained a name for itself in the industry. People
are using it for production environment as well as for academic research papers too. This framework is developed and  maintained by Facebook, another
tech giant.
It uses dynamic graphs ie. graphs are generated on the go while running code. And one can generate the graphs at any point of session afterwards.
Developers at facebook worked really hard to make pytorch more pythonic. This resulted in a faster framework with a lot more control over whatever 
one is doing.
