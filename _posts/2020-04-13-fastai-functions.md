---
layout: post
title: Explanation for fastai api
date: 2020-04-13
tags: [deep learning]
image: images/fastai.png

---


# Language Model
`
learner = language_model_learner(data_lm,AWD_LSTM,drop_mult=0.1,path = opath)
`

This is the first stage of training, where we use the pre-trained language model weights. We are creating a learner model, *learner* that will learn our data. When we create a learner, we have to pass in two things:
* The data: our language model data (data_lm)
* A pre-trained model: here, the pre-trained model is the Wikitext 103 model that will be downloaded for you from fastai.

**drop_mult** , a hyper-parameter ,used for regularization, sets the amount of dropout. If the model is over-fitting increase it, if under-fitting, you can decrease the number.

# Training the model
`learner.fit_one_cycle(1e-2)`

We start training the model with learning rate 1e-2 using fit_one_cycle.

fast.ai library uses latest techniques from deep learning research and one cycle learning is from one of the recent paper and turned out to be both more accurate and faster than any previous approach. First argument ‘1’ is number of epoch runs . We get an accuracy of 29% after running just one epoch.
It trained last layers and basically left most of the model exactly as it was. But what we really want is to train the whole model. 

`learner.unfreeze()`

Normally after we fine-tune the last layers, the next thing we do is we go unfreeze (unfreeze the whole model for training) and train the whole thing.

# Predicting with Language Model

`learner.predict("some random shit", 10)`

To evaluate our language model, we can now run learn.predict and pass in the start of a sentence and specify the number of words we want it to guess.That is pretty decent response and looks like correct grammar. After fine-tuning we get a model that’s good at understanding movie reviews and we can fine-tune that with transfer learning to classify movie reviews to be positive or negative. Let us save the encoding of the model to be used later for classification.

# Encoder
`learn.save_encoder('fine_enc')`

The part of the model that has the understanding of the sentence is called the encoder. So we save it to later use it during the classification stage.

# Creating the classifier
`data_clas = TextClasDataBunch.from_df('./', train_df=df_trn, valid_df=df_val, vocab=data_lm.train_ds.vocab, bs=32)`

Now we’re ready to create our classifier. Step one, is to create a data bunch, TextClasDataBunch, passing the vocab from the language model to make sure that this data bunch is going to have exactly the same vocab. Batch size bs to be used is according to the GPU memory you have available, for a 16GB GPU around bs=64 will work fine. You can find whatever batch size fits on your card and use it accordingly.


`classifier = text_classifier_learner(data_clas, drop_mult=0.5)
classifier.load_encoder('fine_enc')
`


Finally we will create a text classifier learner. Load in our pre train model, the encoding part we saved earlier ‘fine_enc’.
