# FashionMNIST

## 
1. Enhanced Model Architecture did not improve the validation accuracy

I asked perplexity how to increase the validation accuracy, and it recommended to enhance the model architecture.
However, the accuracy dropped as below.
Changes:

Increased layer sizes (512 → 256 → 128) for better feature extraction.

Swish activation (x⋅σ(x)x⋅σ(x)) instead of ReLU for smoother gradients.

Added L2 regularization (λ=0.001) to prevent overfitting.

Batch normalization after each dense layer for stable training.

Higher dropout rate (0.5) to enforce robust learning.

Before:
![image](https://github.com/user-attachments/assets/938b9117-baf8-4d7c-ba32-313e64fe79a2)
![image](https://github.com/user-attachments/assets/d117db86-5b34-4135-a376-d28d2e5d32cb)

After:
![image](https://github.com/user-attachments/assets/381ef769-c2fb-44ba-87d4-c560c871bcf1)
![image](https://github.com/user-attachments/assets/94c8b7af-0aad-45dc-92c0-23d52763e21e)
