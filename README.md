# TreeCaps: Tree-Structured Capsule Networks for Program Source Code Processing.

<p aligh="center"> This repository contains the code for TreeCaps introduced in the following paper 
**TreeCaps: Tree-Structured Capsule Networks for Program Source Code Processing** (NeurIPS Workshops 2019) </p>

[Vinoj Jayasundara](https://scholar.google.com.sg/citations?user=2yTeZ58AAAAJ&hl=en&oi=ao), [Nghi Duy Quoc Bui](https://scholar.google.com/citations?user=QwybxYsAAAAJ&hl=en&oi=ao), [Lingxiao Jiang](https://scholar.google.com/citations?user=0hssXLPZL2YC&hl=en&oi=ao), [David Lo](https://scholar.google.com/citations?user=Ra4bt-oAAAAJ&hl=en&oi=ao)

## Contents
1. [Introduction](#introduction)
2. [Usage](#usage)
3. [Performance](#performance)
4. [Contact](#contact)

## Introduction
<p align="justify"> Program comprehension is a fundamental task in software development and main-tenance processes. Software developers often need to understand a large amount ofexisting code before they can develop new features or fix bugs in existing programs. Being able to process programming language code automatically and provide summaries of code functionality accurately can significantly help developers to reducetime spent in code navigation and understanding, and thus increase productivity. Different from natural language articles, source code in programming languages often follows rigid syntactical structures and there can exist dependencies among code elements that are located far away from each other through complex control flows and data flows. Existing studies on tree-based convolutional neural networks(TBCNN) and gated graph neural networks (GGNN) are not able to capture essential semantic dependencies among code elements accurately. In this paper, we propose novel tree-based capsule networks (TreeCaps) and relevant techniques for processing program code in an automated way that encodes code syntacticalstructures and captures code dependencies more accurately. Based on evaluation onprograms written in different programming languages, we show that our TreeCaps-based approach can outperform other approaches in classifying the functionalitiesof many programs. </p>

Our system comprises three main steps as follows:

<p align="center"><img src="https://www.dropbox.com/s/hxdb8fj50tao9g5/1.eps?dl=0"></p>
<p align="center">(a) TreeCaps approach Overview. The source codes are parsed, vectorized and fed into the proposed TreeCaps network for the program classification task.</p>

<p align="center"><img src="https://www.dropbox.com/s/4jj1ffshh0ogjh3/sys_block_2_crop.png?dl=0&raw=1"></p>
<p align="center">(b) Generating instantiation parameters and reconstructed images</p>

<p align="center"><img src="https://www.dropbox.com/s/0aiheph4ov68sh9/sys_block_3_crop.png?dl=0&raw=1"></p>
<p align="center">(c) Applying the decoder re-training technique</p>

<p align="center"><img src="https://www.dropbox.com/s/dt5ma39m60z9tr2/sys_block_4_crop.png?dl=0&raw=1"></p>
<p align="center">(d) New image data generation technique</p>

## Usage

1. Install [requirements.txt](https://github.com/vinojjayasundara/treecaps/blob/master/requirements.txt) and the required dependencies ```pip install -r requirements.txt```.

2. Clone this repo: ```git clone https://github.com/vinojjayasundara/treecaps.git```.

3. Download and extract the [dataset](https://drive.google.com/open?id=1qdLNPjlNfGSLm9SdbQE6Me8K7Cp4W_ee) and the pre-trained [embedding](https://drive.google.com/open?id=10QTTj6Abhnpay7UPmDdS8uHPfAlxAq8m).

4. Simply run ```python job.py```.

5. Note the following in the ```job.py``` :

* Set ```training = 1``` for training the model and ```training = 0``` for testing.
* Uncomment the lines ```18-20``` in ```job.py``` to continue training with a reduced learning rate.

## Performance

## We credit
We have used [this](https://github.com/naturomics/CapsNet-Tensorflow) as the base CapsNet implementation and [this](https://github.com/crestonbunch/tbcnn) as the base Tree-based convolution implementation. We thank and credit the contributors of these repositories.

## Contact

vinojjayasundara@gmail.com  
Discussions, suggestions and questions are welcome!
