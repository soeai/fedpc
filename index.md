## Introduction

This page introduces the work of the Federated Deep Learning Framework for Privacy-Preserving project from School of Engineering, Tan Tao University. We carry out the research on federated deep learning to address two major issues in distributed deep learning, i.e., data privacy and communication cost.

* We develop a federated learning framework that consists of a master and a number of workers, which hold their private dataset and contribute to the training of a common model but with private training parameters (e.g., batch size, learning rate). 
* We develop a communication protocol that allows a worker to inform the master about the evolution of the model parameters without revealing any sensitive information. The protocol also minimizes the communication overhead, i.e., the amount of data exchanged among the master and workers during the training process.
* To further reduce the communication cost between master and workers, for each training epoch, we develop a goodness function that quantifies the impact of a private dataset on the global model instance, thus determining how much the parameters of the global model instance should be updated based on the information obtained from the respective training worker.
* We develop a parallel and synchronous training algorithm at the master that invokes the training algorithm on each worker and wait for all the workers completing a training epoch before updating the global model instance.
* We provide a formal analysis of the convergence of the training process as well as the privacy protection of the proposed framework.
* We carry out extensive experiments with two deep learning problems: image classification and image segmentation. We used two existing deep learning models for the experiments: ResNet50 FIXUP trained on CIFAR-10 dataset and U-Net trained on the LGG SegmentationDataset. We compared the performance (i.e., accuracy) and efficiency (i.e., communication overhead) of the proposed framework with an existing work.

### User guide
####  Requirements
* Tensorflow 1.x
* open-ssh 


### Publicationds

Tien-Dung Cao, Tram Truong-Huu, Hien Tran, Khanh Tran, "An Efficient and Privacy-preserving Federated Learning Framework for Deep Neural Networks", submitted to Journal of Systems Architecture, Special Issue on Cyber Security for Internet of Things.

### Support or Contact

For any query or issue, please contact dung.cao@ttu.edu.vn
