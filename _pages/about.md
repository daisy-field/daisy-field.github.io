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
n 2015, Google introduced federated learning (FL) as a solution to address the challenges
related to distributed datasets and insufficient data availability [65]. The goal was to enhance
the prediction accuracy of Google’s keyboard next-word suggestions by learning from input
behaviours of all smartphone users while maintaining their privacy rights [65]. In contrast to
traditional machine learning, where all the data is collected on a central server (see Figure 2.2a),
FL algorithms construct machine learning models using models learned on distributed datasets,
located on separate nodes [65]. Typically, the process starts with training a model on the nodes
with the locally available data. The trained models are then transmitted to a central aggregation
server while maintaining data privacy (see Figure 2.2b). The central server generates a global
model by combining the received node models using an aggregation method. FL could not
only enhance the speed and efficiency of real-time data processing, but also increase security
and privacy by keeping sensitive data closer to its point of origin, thereby reducing the risks of
breaches compared to transmitting large volumes of data over potentially insecure networks. It
also offers significant cost advantages and lower latency, enabling faster responses to security
threats and improving the overall performance of IDS [16].
Formally, in FL, we assume, that there are N nodes in a network, labelled as C1, . . . ,CN , each
processing its own data stream D1, . . . , DN . We define the combined dataset D = D1 ∪ · · · ∪ DN ,
which represents all the data observed on all nodes throughout the entire lifespan of the system.
If a central server would be able to collect D, a global model MG could be trained centrally and
then distributed back to the individual detection nodes. However, in an online learning scenario
for learning an intrusion detection model in a heterogeneous network, this would require the
continuous transmission of all data samples to the central server, violating privacy laws and
exceeding the available bandwidth, resulting in inefficiency and slow overall performance.

Intrusion Detection  
======
An intrusion detection system (IDS) monitors a network or system for malicious behaviour
[14, 64]. Based on the location of an IDS, researchers distinguish between two types: Host-
based intrusion detection systems (HIDS) that monitor and analyze the internals of a device,
and network-based intrusion detection systems (NIDS) that monitor and analyze the network
traffic between devices [20]. HIDS operate on individual hosts or devices, observing log files,
file modifications and system activity data. Thereby, an HIDS is also able to detect insider
threats, unauthorized changes, and anomalies that NIDS systems might miss, as NIDS solely
monitor and analyze network traffic transferred between multiple devices in the network. By
investigating network packets, log files, and device activities, NIDS are able to detect a wide
range of network attacks, including unauthorized access, malware, and DDoS attacks [6]. Fur-
thermore, by recognizing suspicious network traffic, for example, through pattern analysis or
advanced machine learning mechanisms, they are more suitable for detecting large-scale or co-
ordinated attacks across the whole network. In this thesis, we will focus on NIDS, however,
the effectiveness of the NIDS can be reduced by encrypted traffic and high-speed networks.
Therefore, we also want to evaluate the system’s capability of training with large volumes of
possibly encrypted network monitoring data and real-time processing in chapter 5.
Besides their location of operation, IDS can be classified into two detection categories:
Signature- and anomaly-based [62]. 

Signature Based IDS
------
In signature-based detection systems, the signature patterns of malicious behaviours are learned based on past activities and stored in a signature
database [102]. When a new signature matches with the signature of a previous, in the database
existing intrusion, an alarm signal is triggered [62]. Signature-based IDS usually have a high
detection accuracy for previously known intrusions, however, these systems are not able to de-
tect malicious zero-day attacks, are often time-consuming and require a high level of domain
expertise to maintain the database with up-to-date signatures [41, 129].


Anomaly Based IDS 
------
In contrast, anomaly-based systems are much more reliable when it comes to unknown,
sophisticated attacks, but might suffer from a higher false alarm rate [12, 41, 62]. An anomaly
based IDS creates a normal model of the behaviour of a computer system or network, e.g. using
machine learning, statistical-based or knowledge-based methods, and detects deviations from
this normal behaviour [62]. Thereby, these highly effective, automated and intelligent anomaly-
based IDS are able to analyze vast amounts of data in real-time, and even adapt to new patterns.
By using incremental machine-learning techniques continuously adapting the model to new
conditions and data patterns [128], these systems can learn from past incidents and adjust to
new types of network traffic to ensure they remain effective in the evolving threat landscape
[69]. Anomalies themselves can be categorized into three types: Point anomalies, contextual
anomalies, and collective anomalies [20].



