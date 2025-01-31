---
layout: archive
title: "Datasets"
permalink: /datasets/
author_profile: true
redirect_from:
  - /resume
---

{% include base_path %}

Attack Simulation Tool
======



March23
======
The first dataset was collected in March 2023 on two road-side
units (RSUs) Cohda MK5 boxes. The dataset was collected with tcpdump5 and contains vari-
ous different information, e.g. map data, traffic light data, messages concerning vehicles, en-
vironmental information and messages containing geo-networking data. In the attack scenario,
the attacker gained physical access to Cohda Box 5 and tried to invade the connected Cohda
Box 2 using Patator6, a tool for multi-purpose brute-forcing and NMAP scans7. The attacker
started by installing the attack tool on Codha Box 5 and scanning of all unprotected ports of
Cohda Box 2, followed by a brute force attack to obtain secure shell (SSH) credentials. After
gaining access, the attacker used their privileges to steal data from the Cohda Box 2. A detailed
description of the anomalies, together with the timestamps, the node that was affected, and the
used protocols and IP addresses, can be found in Table 4.1. In total, the dataset contains almost
500,000 data points for each node, where each sample contains 65 features that we use for
anomaly detection and the training of the underlying intrusion detection model.


DSFIDS24
======
We use the real-world ITS dataset DSFIDS24
[2] collected for training and evaluating network-based intrusion detection systems and avail-
able on GitHub8. The dataset was live captured by Jonathan Ackerschewski [2] in July 2024,
containing data from eight extended-road-side unit (eRSU) devices (node 1 to node 8) from
the BeIntelli infrastructure and one additional device in the network that was assumed to be
controlled by the attacker. The captured datasets contain 24 hours of network traffic and in
total over 24 million packets. The traffic was automatically processed, filtered, and labelled
according to the MITRE ATT&CK® Matrix9. The datasets features attacks such as port scans,
secure shell (SSH) brute-force, discovery, exfiltration, privilege escalation, resource develop-
ment, and multiple DoS attacks, and were executed following a detailed, predefined scenario
depicted in Table 4.2. In an extensive evaluation and analysis, Ackerschewski [2] showed that
the generated dataset closely mirrors real-world vehicular network traffic while containing ac-
curately labelled malicious activities. The combination of diverse attack types and background
traffic ensures a balanced and realistic dataset suitable for the development and benchmarking
of network-based intrusion detection systems in vehicular networks.


  
