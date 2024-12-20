# ViT
2010.11929v2: AN IMAGE IS WORTH 16X16 WORDS


The idea is to divide the picture into pieces like different frames or "tokens" (like tokens in LLM), we convert them to vectors, pass them through a flatten FF network with no activation function. Then we add a positional vectors to those token vectors and pass the result into encoders.  
![image](https://github.com/user-attachments/assets/7c641bfe-50d3-49d7-86e6-70aad97ebaaf)
