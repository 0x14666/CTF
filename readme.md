# CTF: Hybrid Multi-scale Contrastive Transformer for Website Fingerprinting Attack

## Introduction
Website Fingerprinting (WF) attacks, a methodology that allows observers to infer visited websites through encrypted traffic analysis, are usually employed for evaluating the security of anonymous networks like Tor. Although deep learning-based methods have demonstrated significant success in recent studies, existing approaches exhibit limitations. They are insufficient in modeling the intricate characteristics of traffic patterns, which leads to compromised accuracy in identifying challenging samples.

To address these limitations, we propose CTF, a novel WF attack comprising three key components:
1. Extraction of Hybrid Multi-scale Traffic Features (HMTF) integrating spatio-temporal information
2. A novel deep learning framework that synergizes CNN for spatial pattern recognition and Transformer for temporal dependency modeling within HMTF
3. A supervised contrastive learning mechanism to enhance discriminative capability across website fingerprints

Experimental evaluations across multiple benchmark datasets reveal that CTF achieves 99.09% accuracy in Closed-World scenarios, showing enhanced robustness against four SOTA WF defense mechanisms.

## Datasets

| Dataset | # of monitored websites | # of instances | Intro |
|---------|-------------------------|----------------|-------|
| CW.npz | 95 | 105730 | Closed-world dataset. [Details](https://dl.acm.org/doi/pdf/10.1145/3243734.3243768) |
| OW.npz | 95 | 146446 | Open-world dataset. [Details](https://dl.acm.org/doi/pdf/10.1145/3243734.3243768) |
| WTF-PAD.npz | 95 | 105730 | Dataset with WTF-PAD defense. [Details](https://arxiv.org/pdf/1512.00524) |
| Front.npz | 95 | 95000 | Dataset with Front defense. [Details](https://www.usenix.org/system/files/sec20-gong.pdf) |
| Walkie-Talkie.npz | 100 | 90000 | Dataset with Walkie-Talkie defense. [Details](https://www.usenix.org/system/files/conference/usenixsecurity17/sec17-wang-tao.pdf) |
| TrafficSliver.npz | 95 | 95000 | Dataset with TrafficSliver defense. [Details](https://sebastianreuter.info/publications/pdf/ccs-trafficsliver.pdf) |

Quick Download from WFlib storage: https://zenodo.org/records/13732130

## Requirements
- Python 3.8
- PyTorch 2.0.1

## Acknowledgments
We would like to thank the authors of WFlib for their open-source library that facilitates rapid reproduction of previous work:

[Website-Fingerprinting-Library (WFlib)](https://github.com/Xinhao-Deng/Website-Fingerprinting-Library): A PyTorch-based open-source library for website fingerprinting attacks, intended for research purposes only. Website fingerprinting is a type of network attack in which an adversary attempts to deduce which website a user is visiting based on encrypted traffic patterns, even without directly seeing the content of the traffic.

