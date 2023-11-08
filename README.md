# STRIP-AI-Image-Classification-of-Stroke-Blood-Clot-Origin
Silver Solution (48th) for Kaggle Challenge: Image Classification of Stroke Blood Clot Origin 

This is the solution for Mayo Clinic Image Classification challenge that tries to classify the blood clot origins in ischemic stroke. Using whole slide digital pathology images, the challenge aims to build a model that differentiates between the two major acute ischemic stroke (AIS) etiology subtypes: cardiac and large artery atherosclerosis.

I used CoatNet architecture with Focal Loss as the training metric, adamW optimizer wih weight decay to find an optimal solution. The model uses an unconventional architecture version of the CoAtNet and 512 x 512 image size. 

More information about CoatNets can be found here: https://arxiv.org/pdf/2106.04803.pdf 

num_blocks = [2, 2, 4, 8, 2]
channels = [192, 256, 512, 1024, 3072]

