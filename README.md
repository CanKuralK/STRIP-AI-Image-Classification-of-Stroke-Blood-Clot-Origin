# STRIP-AI: Image Classification of Stroke Blood Clot Origin

## Introduction
This repository contains the Silver Solution (48th) for the Kaggle Challenge: Image Classification of Stroke Blood Clot Origin, hosted by the Mayo Clinic. The challenge focuses on classifying the origins of blood clots in ischemic strokes using digital pathology images.

## Objective
The aim is to build a model that differentiates between the two major acute ischemic stroke (AIS) etiologies: cardiac and large artery atherosclerosis, utilizing a novel approach in medical image classification.

## Methodology
My approach leverages a modified version of the CoAtNet architecture, with a focal point on using Focal Loss as the training metric and AdamW optimizer with weight decay for optimal performance. The image inputs are standardized to a size of 512 x 512 pixels.

## Architecture

### CoAtNet: Marrying Convolution and Attention for All Data Sizes

The CoAtNet paper attempts to effectively combine the strengths from both convolutional and transformers architectures, they present CoAtNets(pronounced "coat" nets), a family of hybrid models built from two key insights: 
- Depthwise Convolution and self-Attention can be naturally unified via simple relative attention
- Vertically stacking convolution layers and attention layers in a principled way is surprisingly effective in improving generalization, capacity and efficiency.

![](https://i.ibb.co/Sd6wj7D/Selection-998.png)

The CoAtNet model is structured as follows:
- Number of Blocks: [2, 2, 4, 8, 2]
- Channels: [192, 256, 512, 1024, 3072]

## Results
Here are the visual results from the manuscript, showcasing the model's performance and the differentiation of clot origins.

Epoch 5/5 | train | Loss: 0.6523 | Acc: 0.6697
Epoch 5/5 |  val  | Loss: 0.6896 | Acc: 0.5479

## Conclusion
The implemented CoAtNet architecture with Focal Loss has proven to be effective in distinguishing between cardiac and large artery atherosclerosis strokes, holding potential for real-world clinical applications.

## References
- CoAtNet Paper : https://arxiv.org/pdf/2106.04803.pdf
- Kaggle Challenge Link : https://www.kaggle.com/competitions/mayo-clinic-strip-ai/overview
- Any other libraries or tools used : einops 

## Contact/Contribution
Feel free to contribute to this project by forking the repository and submitting a pull request. If you have any questions or would like to discuss the project further, please reach out via kkural@gmu.edu


