# SciPy 2018

## Title:

### cis_interface: A Python package for connecting scientific models across scales and languages

## Keywords:
scientific modeling
biology
parallel processing
message passing
simulations

## Abstract:

(Around 100 words; this will be used a the summary of your talk in the online program.)

In this talk we describe cis_interface, an open-source Python framework for combining scientific 
models across programming languages and scales to simulate complex systems. Motivated by the goal 
of combining biological models to recreate crops in silico, cis_interface orchestrates asynchronous 
communication between models running in parallel without the need for major changes to the model code, 
supporting scientific collaboration and leveraging the wealth of existing computational models. 

## Extended Abstract:

(Should be no more than 2 pages, and address the following: Do you intend to present a demo? Does the 
work make any new contributions to open-source software? Which existing open-source tools does it use? 
What science fields are impacted by the work? How does it work fit into the Scientific Python community?)

This talk will cover the motivation and structure of the cis_interface framework, a new open-source 
Python package. Although applicable to any network of scientific models, the cis_interface package was 
originally designed to combine computational plant biology models. The plant biology community has 
produced a wealth of computational models for biological processes contributing to plant growth from 
genetic regulatory networks to photosynthesis to plant and field level structure. While each model is 
limited to a narrow scope on its own, focussing on a specific scale and scientific question, they are 
dependent on properties of the plant at other scales. Therefore, it should be possible to create a 
network of such models, linking the output from one to the input of the other. However, these models 
are usually developed independently by groups at different institutions without the initial intention 
to be combined with another model. As a result, the models may be in different programming languages or 
use different data structures and can be difficult to combine. Either major changes must be made to the 
code base of one and/or both models or the exchange of information must be done manually, creating a 
significant barrier to scientists, particularly those early in their career. The challenge of combining 
models becomes even more difficult when the models are iterative and must be run many times with 
information exchanged between each run. The cis_interface packages tackles this challenge.

We will discuss the different message passing schemes offered by cis_interface to facilitate asynchronous 
communication between models in different programming languages including use of the ZeroMQ, RabbitMQ, 
and System V Python packages (pyzmq, pika, sysv_ipc). In addition to these packages, the cis_interface 
package utilizes several open source Python projects including scipy, numpy, and astropy. We will also 
discuss the mindset behind the cis_interface package. In order to lower the barrier to entry for early 
career domain scientists and encourage adoption, we have designed the cis_interface to be minimally 
invasive to the model code with little need to be aware of the underlying communication and model 
orchestration.

This talk is intended for domain scientists interested in combining computational models and will expand 
on the lightning talk I gave on the cis_interface at SciPy 2017.

Relevant Links:
Source code: https://github.com/cropsinsilico/cis_interface
Documentation: https://cropsinsilico.github.io/cis_interface/
