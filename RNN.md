## Recurrent Neural Network

![image](https://user-images.githubusercontent.com/79006607/153572542-39cee877-f213-406d-87e2-ceeaa0f0a8cc.png)
- The principle advantage of RNNs is that they propagate information within sequences and your computation's share most of the parameters.
- the information from every word in the sequence is multiplied by the same weights, Wx. The information propagated from the beginning to the end is multiplied by Wh.
- the block is repeated for every word in the sequence. They compute values that are fed over and over again to themselves until a prediction is made
- The only learnable parameters are the ones in Wx, Wh, and W, the weights used to make the final prediction. That's why they're called recurrent neural networks. 
- As you feed in more information into the model, the previous word's retention gets weaker, but it is still there.


### Applications of RNN:
#### One to One: 
- Ex.  Given some scores of a championship, you can predict the winner. 

#### One to Many:
- Ex. Giving a Image and generating caption for the image.

#### Many to One:
- Ex. Sentiment Analysis: Giving a tweet and predicting +ve or -ve sentiment

#### Many to Many:
- Ex. Language translation


### Math of Simple RNN
![image](https://user-images.githubusercontent.com/79006607/153581458-ddcf92b6-aa55-48b1-9faf-11ce0e815397.png)



### Significance of RNN or How RNN is different from feedforward network or Convolution network?
- Account for dependence between inputs
- Account for variable number of Inputs
- It make sure that function executed at each time step/ variable inputs is the same


### Advantages of TRAX:
- Runs fast on CPUs, GPUs and TPUs
- Parallel computing
- Record algebraic computations for gradient evaluation
- Runs on the top of Tensorflow

![image](https://user-images.githubusercontent.com/79006607/153556623-a0734e5c-03a6-4bfa-863c-4010f54612c0.png)

Official Trax documentation maintained by the Google Brain team:
https://trax-ml.readthedocs.io/en/latest/

Trax source code on GitHub:
https://github.com/google/trax
