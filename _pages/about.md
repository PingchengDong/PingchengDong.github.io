---
permalink: /
title: ""
excerpt: ""
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

{% if site.google_scholar_stats_use_cdn %}
{% assign gsDataBaseUrl = "https://cdn.jsdelivr.net/gh/" | append: site.repository | append: "@" %}
{% else %}
{% assign gsDataBaseUrl = "https://raw.githubusercontent.com/" | append: site.repository | append: "/" %}
{% endif %}
{% assign url = gsDataBaseUrl | append: "google-scholar-stats/gs_data_shieldsio.json" %}

<span class='anchor' id='about-me'></span>

I am a final-year PhD candidate in the Department of Electronic and Computer Engineering at the [Hong Kong University of Science and Technology (HKUST)](https://hkust.edu.hk/) and the [AI Chip Center for Emerging Smart Systems (ACCESS)](https://inno-access.hk/). I am a member of the [Vision and System Design Lab (VSDL)](https://vsdl.hkust.edu.hk/index.html), supervised by [Prof. Kwang-Ting CHENG](https://seng.hkust.edu.hk/about/people/faculty/tim-kwang-ting-cheng). I obtained my BEng degree in Microelectronic Science and Engineering from the [Southern University of Science and Technology (SUSTech)](https://www.sustech.edu.cn/en/) in 2022. My research focuses on hardware-software co-design, 3D IC, Design-Technology Co-Optimization (DTCO), and hardware-aware model compression. More details can be found in my [CV](/images/pingcheng_dong_cv.pdf). Feel free to reach out if you are interested in collaboration or discussion.<br>
E-mail: pingcheng.dong@connect.ust.hk \| WeChat: PN-Junction

<!-- My research interest includes neural machine translation and computer vision. I have published more than 100 papers at the top international AI conferences with total <a href='https://scholar.google.com/citations?user=DhtAFkwAAAAJ'>google scholar citations <strong><span id='total_cit'>260000+</span></strong></a> (You can also use google scholar badge <a href='https://scholar.google.com/citations?user=DhtAFkwAAAAJ'><img src="https://img.shields.io/endpoint?url={{ url | url_encode }}&logo=Google%20Scholar&labelColor=f6f6f6&color=9cf&style=flat&label=citations"></a>).
 -->
<span class="anchor" id="honors"></span>

# 🎖 Honors and Awards
- *2022* Outstanding Graduate (Top 8 in the College of Engineering, SUSTech) 
- *2021* China National Scholarship (Top 8 in SUSTech)
- *2021* Scientific Research Star (Top 1 in Shuren College, SUSTech)
- *2020* The First Prize of Outstanding Students in SUSTech (Top 5% in SUSTech)
- *2019* The Second Prize of Outstanding Students in SUSTech (Top 10% in SUSTech)

<span class="anchor" id="publications"></span>

# 📝 Selected Publication

<div class='paper-box paper-box-shared'>
<div class='paper-box-image'><img src='images/rhb_2026.png' alt="ReRAM-on-logic stacked chip, four-chip system, and SEM/TEM images" width="100%"></div>
<div class='paper-box-text' markdown="1">

[RS-LPU: A ReRAM-on-Logic Stacked Large Language Model Accelerator with Software-Hardware Co-Designed Weight Compression and Speculative Decoding](https://doi.org/10.1109/JSSC.2026.3718555)

**Pingcheng Dong**, Yonghao Tan, Xuejiao Liu, Peng Luo, Yu Liu, Di Pang, Fengshi Tian, Songchen Ma, Xijie Huang, Shih-Yang Liu, Dong Zhang, Zhichao Lu, Luhong Liang, Chi-Ying Tsui, Fengbin Tu, Liang Zhao, Kwang-Ting Cheng.

**2026**, *IEEE Journal of Solid-State Circuits (JSSC)*

<hr class="paper-entry-divider">

[A 14.08-to-135.69 Token/s ReRAM-on-Logic Stacked Outlier-Free Large-Language-Model Accelerator with Block-Clustered Weight-Compression and Adaptive Parallel-Speculative-Decoding](https://ieeexplore.ieee.org/abstract/document/11409211)

**Pingcheng Dong**, Yonghao Tan, Xuejiao Liu, Peng Luo, Yu Liu, Di Pang, Songchen Ma, Xijie Huang, Shih-Yang Liu, Dong Zhang, Zhichao Lu, Luhong Liang, Chi-Ying Tsui, Fengbin Tu, Liang Zhao, Kwang-Ting Cheng.

**2026**, *IEEE International Solid-State Circuits Conference (ISSCC)*

</div>
</div>


<div class='paper-box'><div class='paper-box-image'><div><img src='images/2024_ISSCC_v2.png' alt="sym" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

[A 28nm 0.22μJ/Token Memory-Compute-Intensity-Aware CNN-Transformer Accelerator with Hybrid-Attention-Based Layer-Fusion and Cascaded Pruning for Semantic-Segmentation](https://ieeexplore.ieee.org/abstract/document/10904499)

**Pingcheng Dong**<sup>*</sup>, Yonghao Tan<sup>*</sup>, Xuejiao Liu, Peng Luo, Yu Liu, Luhong Liang, Yitong Zhou, Di Pang, Manto Yung, Dong Zhang, Xijie Huang, Shih-Yang Liu, Yongkun Wu, Fengshi Tian, Chi-Ying Tsui, Fengbin Tu, Kwang-Ting Cheng.

<em>*: Equal contribution</em>

**2025**, *IEEE International Solid-State Circuits Conference (ISSCC)*

</div>
</div>


<div class='paper-box'><div class='paper-box-image'><div><img src='images/apsq_2025.png' alt="APSQ algorithm-hardware co-design overview" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

[APSQ: Additive Partial Sum Quantization with Algorithm-Hardware Co-Design](https://arxiv.org/abs/2505.03748)

Yonghao Tan<sup>*</sup>, **Pingcheng Dong**<sup>*</sup>, Yongkun Wu, Yu Liu, Xuejiao Liu, Peng Luo, Shih-Yang Liu, Xijie Huang, Dong Zhang, Luhong Liang, Kwang-Ting Cheng.

<em>*: Equal contribution</em>

**2025**, *62nd ACM/IEEE Design Automation Conference (DAC)*

</div>
</div>


<div class='paper-box'><div class='paper-box-image'><div><img src='images/DAC_GQA.png' alt="sym" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

[Genetic Quantization-Aware Approximation for Non-Linear Operations in Transformers](https://doi.org/10.1145/3649329.3657314)

**Pingcheng Dong**<sup>*</sup>, Yonghao Tan<sup>*</sup>, Dong Zhang, Tianwei Ni, Xuejiao Liu, Yu Liu, Peng Luo, Luhong Liang, Shih-Yang Liu, Xijie Huang, Huaiyu Zhu, Yun Pan, Fengwei An and Kwang-Ting Cheng.

<em>*: Equal contribution</em>

**2024**, *61st ACM/IEEE Design Automation Conference (DAC)*

</div>
</div>


<div class='paper-box'><div class='paper-box-image'><div><img src='images/esscirc.png' alt="sym" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

[A 1920×1080 129fps 4.3pJ/Pixel Stereo-Matching Processor for Pico Aerial Vehicles](https://ieeexplore.ieee.org/document/10268790)

**Pingcheng Dong**, Zhuoyu Chen, Ke Li, Lei Chen, Kwang-Ting Cheng, Fengwei An. 

**2023**, *IEEE 49th European Solid State Circuits Conference (ESSCIRC)*

</div>
</div>

<div class='paper-box'><div class='paper-box-image'><div><img src='images/tcas1.gif' alt="sym" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

[A 4.29 nJ/pixel stereo depth coprocessor with pixel level pipeline and region optimized semi-global matching for IoT application](https://ieeexplore.ieee.org/abstract/document/9505253)

**Pingcheng Dong**<sup>*</sup>, Zhuoyu Chen<sup>*</sup>, Zhuoao Li, Yuzhe Fu, Lei Chen, Fengwei An.  

<em>*: Equal contribution</em>

**2021**, *IEEE Transactions on Circuits and Systems I: Regular Papers*

</div>
</div>


# 📝 Collaborative Publications

- [ProQuant: Progressive Quantization-aware Training for Edge MLLMs](https://arxiv.org/abs/2611.08216). Yufei Xue, Yushi Huang, Jiawei Shao, **Pingcheng Dong**, Yonghao Tan, Shiyao Li, Kwang-Ting Cheng, Jun Zhang. **2026**, *Conference on Neural Information Processing Systems (NeurIPS)*

- [A 5nm 91.43 TOPS/W 4-Chiplet Generalizable-Rendering-Processor with UCIe-Enabled Cross-Die-Cache and Balance-Aware Progressive Multi-Level Sparsity](https://doi.org/10.1109/CICC65509.2026.11509482). Yonghao Tan, Songchen Ma, **Pingcheng Dong**, Peng Luo, Zhiyuan Lei, Wencai Lu, Guangxi Ying, Man-To Yung, Haibo Zhao, Lan Liu, Yuzhong Jiao, Xuejiao Liu, Yu Liu, Li Li, Luhong Liang, Mao Liu, Kwang-Ting Cheng. **2026**, *IEEE Custom Integrated Circuits Conference (CICC), pp. 1–4*

- [Expert Streaming: Accelerating Low-Batch MoE Inference via Multi-chiplet Architecture and Dynamic Expert Trajectory Scheduling](https://arxiv.org/abs/2603.27624). Songchen Ma, Hongyi Li, Weihao Zhang, Yonghao Tan, **Pingcheng Dong**, Yu Liu, Lan Liu, Yuzhong Jiao, Xuejiao Liu, Luhong Liang, Kwang-Ting Cheng. **2026**, *IEEE International Symposium on High-Performance Computer Architecture (HPCA)*

- [Cyclic Contrastive Knowledge Transfer for Open-Vocabulary Object Detection](https://proceedings.iclr.cc/paper_files/paper/2025/hash/b8f10193cab43d45df9bb810637333fd-Abstract-Conference.html). Chuhan Zhang, Chaoyang Zhu, **Pingcheng Dong**, Long Chen, Dong Zhang. **2025**, *International Conference on Learning Representations (ICLR)*

- [Memory Efficient Transformer Adapter for Dense Predictions](https://arxiv.org/abs/2502.01962). Dong Zhang, Rui Yan, **Pingcheng Dong**, Kwang-Ting Cheng. **2025**, *International Conference on Learning Representations (ICLR)*

- [Quantization Variation: A New Perspective on Training Transformers with Low-Bit Precision](https://arxiv.org/abs/2307.00331). Xijie Huang, Zhiqiang Shen, **Pingcheng Dong**, Kwang-Ting Cheng. **2024**, *Transactions on Machine Learning Research (TMLR)*

- [LLM-FP4: 4-Bit Floating-Point Quantized Transformers](https://arxiv.org/abs/2310.16836). Shih-Yang Liu, Zechun Liu, Xijie Huang, **Pingcheng Dong**, Kwang-Ting Cheng. **2023**, *Conference on Empirical Methods in Natural Language Processing (EMNLP), Main Conference*

# 😀 Teaching Assistant
- ELEC3400 Introduction to Integrated Circuits and Systems (2023 Spring)
- ELEC4320 FPGA based Design: From Theory to Practice (2023 Fall)



  
  



