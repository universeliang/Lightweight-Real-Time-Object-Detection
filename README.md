# Title
Lightweight Real-Time Object Detection via Enhanced Global Perception and Intra-Layer Interaction for Complex Traffic Scenarios

# Abstarct
Due to unfavorable factors such as cluttered spatial and temporal distribution of multiple types of targets, occlusion of background objects of different shapes, and blurring of feature information by inclement weather, the low detection accuracy in complex traffic scenarios has been a troubling issue. Regarding the above-mentioned issues, the paper proposes a lightweight real-time detection network to augment multi-scale object perception capabilities in traffic scenarios while ensuring real-time detection speed. First, we construct a novel global feature extraction (GFE) structure by cascading orthogonal band convolution kernels that capture the global dependencies between pixels to improve feature discrimination. Then, an intra-layer multi-scale feature interaction (IMFI) module is proposed to reinforce the effective reuse and multi-level transfer of salient features. In addition, we build a multi-branch scale-aware aggregation (MSA) module that captures abundant context-associated features to improve the target decision-making capability and the self-adaptive capability of the model when dealing with diverse object scales. Experimental results demonstrate that the proposed approach attains a significant improvement of 5.6 percentage points in AP50 with fewer parameters and computational power compared to the baseline model, with an improved FPS of 73. Furthermore, our approach strikes the optimal speed-accuracy balance when compared against other excellent object detection algorithms of the same magnitude.

# Tips
Thank you all for your interest in our work. Here is our project repository containing the source code and relevant materials. We encourage you to review its contents thoroughly and should you encounter any questions, or issues, or require assistance, please do not hesitate to contact us promptly.

This repository holds the implementation details corresponding to our article addressing ['Traffic Object detection']. It encompasses the codebase that we have developed and utilized throughout our research, along with essential datasets and documentation.

# Model Train Start

## train.py
In this repository, the train.py script serves as the core training module for our model. By directly executing this file, users can initiate the model training process. The script comprehensively includes several key configurable parameters such as the number of epochs for training, batch size for input data processing, and various optimization settings.

## val.py
The val.py script serves as a pivotal part of the project, aimed at assessing the quality and robustness of the trained model. Upon completion of the training phase, running this script will apply the trained model to a held-out validation set or test set. It typically measures various metrics pertinent to the specific problem domain, such as accuracy, precision, recall, F1 score, or mean squared error, depending on whether the task is classification or regression-based.

## detect.py
The detect.py script within this repository is specifically designed for testing the trained model in practical scenarios.

# Model Structure
Within the repository, the overall architecture of the proposed model, along with its key components - GFE, IMFI, and MSA modules - are implemented in the models/common.py file. These modules represent the innovative aspects of our model design that aim to improve its feature extraction and representation capabilities.

For specific details regarding the channel numbers, stacking layers, and positional arrangements of these modules, please refer to the yolov5s_fog_cityscapes.yaml configuration file. This YAML file serves as a centralized hub for defining the architectural specifications of the model. It provides a clear, structured, and easily editable format for adjusting the network's hyperparameters without having to modify the code directly.
