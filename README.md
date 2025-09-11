# Abstract
Medical image segmentation is a critical task in clinical workflows, particularly for the detection and delineation of
pathological regions. While convolutional architectures like U-Net have become standard for such tasks, their limited
receptive field restricts global context modeling. Recent efforts integrating transformers have addressed this, but often
result in deep, computationally expensive models unsuitable for real-time use. In this work, we present a novel end-to-
end lightweight architecture designed specifically for real-time binary medical image segmentation. Our model combines
a Swin Transformer-like encoder with a U-Net-like decoder, connected via skip pathways to preserve spatial detail
while capturing contextual information. Unlike existing designs such as Swin Transformer or U-Net, our architecture
is significantly shallower and competitively efficient. To improve the encoder’s ability to learn meaningful features
without relying on large amounts of labeled data, we first train it using Barlow Twins, a self-supervised learning method
that helps the model focus on important patterns by reducing unnecessary repetition in the learned features. After
this pretraining, we fine-tune the entire model for our specific task. Experiments on benchmark binary segmentation
tasks demonstrate that our model achieves competitive accuracy with substantially reduced parameter count and faster
inference, positioning it as a practical alternative for deployment in real-time and resource-limited clinical environments.


# Framework

<img width="1809" height="927" alt="image" src="https://github.com/user-attachments/assets/63e1a656-6c81-488c-a95b-c09016530905" />

# Results Comparison on different datasets

<img width="966" height="496" alt="image" src="https://github.com/user-attachments/assets/d6f351ec-75c5-4311-b090-22337c065e1f" />

# A short demo video of real-time blood cell segmentation

https://github.com/user-attachments/assets/a5949779-bef5-47ca-a714-56166d7d52cf


# Arxiv Link
https://arxiv.org/abs/2509.06885
