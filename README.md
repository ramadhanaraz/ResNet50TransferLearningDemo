# **ResNet50 Transfer Learning Demonstration**

## **About**

A simple demonstration for transfer learning method to train ML model faster by utilizing available pretrained models.

## **How does it work?**

There are several variations of this method, but particularly they all follow the same baseline steps.

> ### ***Transfer Learning Basic Steps***
>
> 1. Create a blank new instance of sequential model.
> 2. Loads up a pretrained model on it without the top layer. Generally a top layer on a pretrained models is the last layer that classifies for the original uses case of that particular model. Since we will add our custom layer on top of it later, we won't be needing this.
> 3. Freeze all the layers on the pretrained model then, add it on our blank sequential model. These layers **need** to be freezed so their weight won't be trained again when we fit the model into our dataset.
> 4. Add our custom layers on top of the pretrained model layer. These can be whatever we want depending on the uses case of the model.
> 5. Compile the model with an optimizer of the choice. Finally, train it on your dataset.

## **Why would you want to use it in the first place?**

The biggest advantage of using this method is you could reduce a lot of training times and lift all the heavy work by using a pretrained model weights.

Another advantage of transfer learning is, generally most of these pretrained models are already trained by a huge dataset. Because of that, mostly it will result on a much better fitting model depending on the dataset we fit into.
