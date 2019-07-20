# Variational-Autoencoder-VAE

This is the implementation of VAE for own research purpose

Unlike traditional auto encoders it used variational inference.

Model architecture

encoder 
    1*784===>1*400
    1*400===>1*20 (Bottle Neck layer)
    
decoder
   1*20====>1*400
   1*400===>1*784
   
Please note the loss function consists of two terms 1) reconstruction loss 2) Regularization
model is trying to minimize the both i.e it is minimiizing the KL divergence of the distribution coming out of the encoder and Multivarient Normal Distribution( Mean=0, in covariance matrix only diagonal element are 1 other are fixed to zero.), so we are assuming some dimension of latent variable(int this model 20) and trying the predict the parameters accordingly.



Result

![VAE Result](https://user-images.githubusercontent.com/51395380/61580795-41f88a80-ab33-11e9-9b3b-21a29768a55b.PNG)





