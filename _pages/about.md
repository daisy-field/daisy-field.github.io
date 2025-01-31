---
permalink: /
title: "DAISY Federated Online Learning Framework"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

This is the main page of the Daisy Organization. 
Cybersecurity in modern networks presents significant challenges arising from the heterogeneity of devices, dynamic topology changes, varying computational capabilities, and limited network bandwidth. Highly automated intrusion detection systems (IDS) with integrated machine learning methods became one of the most important defence methods against potential cybersecurity threats, by continuously monitoring network traffic and reporting potential security violations automatically. However, training such machine learning models for the automatic detection of threats is still a challenging task, as the data is heterogeneous, spread across different locations and often non-iid. 
In this project, we conduct a comprehensive evaluation of pFL as a solution for collaborative training of heterogeneous machine learning models on \ac{noniid} data. In contrast to traditional FL, pFL allows us to efficiently optimize the usage of local resources, perfectly adapt the model to the local data distribution and simultaneously improve the overall performance through knowledge exchange with other nodes. We propose and implement two innovative pFL approaches for the application in real-world heterogeneous environments. The first approach trains a GAN used to enrich other node's local training datasets with generated synthetic samples,   
while the second approach benefits from a two-stage, decentralized multi-teacher knowledge distillation technique to transfer the knowledge between completely heterogeneous models. 

 
We evaluate and compare both approaches to traditional FedAVG using the CIC-IDS17 dataset and two real-world ITS datasets containing network data of various cameras, sensors and vehicles, collected on up to eight different road-side locations. 
Additionally, we show that pFL is able to effectively reduce the effect of model poisoning attacks in specific scenarios on the network.
An unexpected drawback of pFL  approaches is the significantly higher computational effort, however, this limitation can be neglected due to the gained possibility to completely customize the local model of a node, which is particularly valuable in  highly heterogeneous networks. 

Federated Learning
======


Intrusion Detection  
======

Signature Based IDS
------


Anomaly Based IDS 
------


**Markdown generator**

The repository includes [a set of Jupyter notebooks](https://github.com/academicpages/academicpages.github.io/tree/master/markdown_generator
) that converts a CSV containing structured data about talks or presentations into individual markdown files that will be properly formatted for the Academic Pages template. The sample CSVs in that directory are the ones I used to create my own personal website at stuartgeiger.com. My usual workflow is that I keep a spreadsheet of my publications and talks, then run the code in these notebooks to generate the markdown files, then commit and push them to the GitHub repository.

How to edit your site's GitHub repository
------
Many people use a git client to create files on their local computer and then push them to GitHub's servers. If you are not familiar with git, you can directly edit these configuration and markdown files directly in the github.com interface. Navigate to a file (like [this one](https://github.com/academicpages/academicpages.github.io/blob/master/_talks/2012-03-01-talk-1.md) and click the pencil icon in the top right of the content preview (to the right of the "Raw | Blame | History" buttons). You can delete a file by clicking the trashcan icon to the right of the pencil icon. You can also create new files or upload files by navigating to a directory and clicking the "Create new file" or "Upload files" buttons. 

Example: editing a markdown file for a talk
![Editing a markdown file for a talk](/images/editing-talk.png)

For more info
------
More info about configuring Academic Pages can be found in [the guide](https://academicpages.github.io/markdown/), the [growing wiki](https://github.com/academicpages/academicpages.github.io/wiki), and you can always [ask a question on GitHub](https://github.com/academicpages/academicpages.github.io/discussions). The [guides for the Minimal Mistakes theme](https://mmistakes.github.io/minimal-mistakes/docs/configuration/) (which this theme was forked from) might also be helpful.
