---
permalink: /
title: "About Me"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

I am a Ph.D. student at the National University of Singapore's School of Computing working under the supervision of [Reza Shokri](https://www.comp.nus.edu.sg/~reza/). My research interests are in the privacy and fairness of machine learning, federated learning and Large Language Models.

## Publications

### Context-Aware Membership Inference Attacks against Pre-trained Large Language Models
*Chang, H., Shahin Shamsabadi, A., Katevas, K., Haddadi, H., & Shokri, R. Context-Aware Membership Inference Attacks against Pre-trained Large Language Models.*

Prior Membership Inference Attacks (MIAs) on pre-trained Large Language Models (LLMs), adapted from classification model attacks, fail due to ignoring the generative process of LLMs across token sequences. In this paper, we present a novel attack that adapts MIA statistical tests to the perplexity dynamics of subsequences within a data point. Our method significantly outperforms prior loss-based approaches, revealing context-dependent memorization patterns in pre-trained LLMs.

### [Watermark Smoothing Attacks against Language Models](https://arxiv.org/abs/2407.14206)
*Chang, H., Hassani, H., & Shokri, R. (2024). Watermark Smoothing Attacks against Language Models. ArXiv Preprint ArXiv:2407.14206.*

Watermarking is a technique used to embed a hidden signal in the probability distribution of text generated by large language models (LLMs), enabling attribution of the text to the originating model. We introduce smoothing attacks and show that existing watermarking methods are not robust against minor modifications of text. An adversary can use weaker language models to smooth out the distribution perturbations caused by watermarks without significantly compromising the quality of the generated text. The modified text resulting from the smoothing attack remains close to the distribution of text that the original model (without watermark) would have produced. Our attack reveals a fundamental limitation of a wide range of watermarking techniques.

### [Efficient Privacy Auditing in Federated Learning](https://www.comp.nus.edu.sg/~hongyan//papers/chang2024efficient.pdf)
*Chang, H., Edwards, B., Paul, A., & Shokri, R. (2024). Efficient Privacy Auditing in Federated Learning. Usenix Security Symposium (USENIX).*

We design a novel efficient membership inference attack to audit privacy risks in federated learning. Our approach involves computing the slope of specific model performance metrics (eg, model's output and its loss) across FL rounds to differentiate members from non-members. Since these metrics are automatically computed during the FL process, our solution imposes negligible overhead and can be seamlessly integrated without disrupting training. We validate the effectiveness and superiority of our method over prior work across a wide range of FL settings and real-world datasets.

### On The Impact of Machine Learning Randomness on Group Fairness
*Ganesh, P., Chang, H., Strobel, M., & Shokri, R. (2023). On The Impact of Machine Learning Randomness on Group Fairness. Proceedings of the 2023 ACM Conference on Fairness, Accountability, and Transparency*

### [Bias Propagation in Federated Learning](https://arxiv.org/abs/2210.11266)
*Chang, H., & Shokri, R. (2023). Bias Propagation in Federated Learning. International Conference on Learning Representations (ICLR).*

### [On the privacy risks of algorithmic fairness](https://ieeexplore.ieee.org/abstract/document/9581257)
*Chang, H., & Shokri, R. (2021). On the privacy risks of algorithmic fairness. 6th IEEE European Symposium on Security and Privacy (Euro S&P).*

### On adversarial bias and the robustness of fair machine learning
*Chang, H., Nguyen, T. D., Murakonda, S. K., Kazemi, E., & Shokri, R. (2020). On adversarial bias and the robustness of fair machine learning. In arXiv.*
