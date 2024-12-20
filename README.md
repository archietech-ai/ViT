# ViT
2010.11929v2: AN IMAGE IS WORTH 16X16 WORDS


The idea is to divide the picture into pieces like different frames or "tokens" (like tokens in LLM), we convert them to vectors, pass them through a flatten FF network with no activation function. Then we add a positional vectors to those token vectors and pass the result into encoders.  
![image](https://github.com/user-attachments/assets/7c641bfe-50d3-49d7-86e6-70aad97ebaaf)


-------------------

### Inductive Bias:

The assumptions we make about our data (like linearality in linear learners)
More assumptions we make, more restrictive and smaller the solution domain is, so the solution is not neccessarly the best answer. More intensive the assumptions, the number of solutions will be restrictive and sub-optimal.

In CNN we also assume some assumption like locality. 

![image](https://github.com/user-attachments/assets/e4d3e51a-1875-4311-a1ff-01cf9c0e5f9a)

