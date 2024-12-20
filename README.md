# ViT
2010.11929v2: AN IMAGE IS WORTH 16X16 WORDS


The idea is to divide the picture into pieces like different frames or "tokens" (like tokens in LLM), we convert them to vectors, pass them through a flatten FF network with no activation function. Then we add a positional vectors to those token vectors and pass the result into encoders.  
![image](https://github.com/user-attachments/assets/7c641bfe-50d3-49d7-86e6-70aad97ebaaf)


-------------------

### Inductive Bias:

![image](https://github.com/user-attachments/assets/e4d3e51a-1875-4311-a1ff-01cf9c0e5f9a)

The assumptions we make about our data (like linearality in linear learners) is cslled Inductive Bias
More assumptions we make, more restrictive and smaller the solution domain is, so the found solution is not neccessarly the best answer. More intensive the assumptions, the number of solutions will be restrictive and sub-optimal.

In CNN we also assume some assumption like locality. When we wanted to find a feature, we use a kernel with specific size (like 3x3) and we use that to find the feature of that image. So we assume the 3x3 pixel around the current position is a good representative (but it could be 5x5 or even entire picture)

In transformers we do not have that much inductive bias. Every frame in this article can access other frames information (through encoder attention). So we do not have locality assumption here, it's more flexible. Hence less "inductive bias". We still have bias, but is less than CNN.

One message of this article is more data we have, transformers are better than CNN. When we have limited data, using more intesive inductive bias finds the solutions better. But if we have lots of data, less inductive bias result a better output.

TRansformers are the most general mochine we have created but they are very data hungry.

#### Pretraining:
ImageNet--> 1 M images and 1000 classes

ImageNet 21 K --> 14 M images and 21 K classes

JFT-303 M ---> Google owned data (not public), It has 303 M images (There is a new data set called JFT-3B too)

#### Fine Tuning:

CFAR 10 and CFAR 100

Oxford

ImageNet (validation data sets)

#### ViT variations:

Same as BERT that has base and large versions, we have differemt variations here:

![image](https://github.com/user-attachments/assets/9b457c7d-0ca5-4820-b1c8-2e75fff87dd3)


#### Performance evaluation:

The performance of the model is based on the data that is used for fine tuning. All the models in the following table use JFT-300M for pre-training.


![image](https://github.com/user-attachments/assets/33f1bca8-d18e-4cd1-b01b-6a346658361f)

BiT-L and Noisy Student are a bit older than ViL and they are CNN based. 


ViT outperform ResNet.

In the first row we see that when model is larger (meaning less inductive bias w ehave) the model can learn better on huge data set compare to smaller data set. ViT-H performs better than ViT-L








