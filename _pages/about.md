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

I am a 4th-year PhD candidate in the Department of Electronic and Computer Engineering at the [Hong Kong University of Science and Technology (HKUST)](https://hkust.edu.hk/) and the [AI Chip Center for Emerging Smart Systems (ACCESS)](https://inno-access.hk/). I am a member of the [Vision and System Design Lab (VSDL)](https://vsdl.hkust.edu.hk/index.html), supervised by [Prof. Kwang-Ting CHENG](https://seng.hkust.edu.hk/about/people/faculty/tim-kwang-ting-cheng). I obtained my BEng degree in Microelectronic Science and Engineering from the [Southern University of Science and Technology (SUSTech)](https://www.sustech.edu.cn/en/) in 2022. My research focuses on hardware-software co-design, 3D IC, Design-Technology Co-Optimization (DTCO), and hardware-aware model compression. More details can be found in my [CV](../images/CanadaCast_CV_example.pdf). Feel free to reach out if you are interested in collaboration or discussion.  
E-mail: pingcheng.dong@connect.ust.hk \| WeChat: PN-Junction

<!-- My research interest includes neural machine translation and computer vision. I have published more than 100 papers at the top international AI conferences with total <a href='https://scholar.google.com/citations?user=DhtAFkwAAAAJ'>google scholar citations <strong><span id='total_cit'>260000+</span></strong></a> (You can also use google scholar badge <a href='https://scholar.google.com/citations?user=DhtAFkwAAAAJ'><img src="https://img.shields.io/endpoint?url={{ url | url_encode }}&logo=Google%20Scholar&labelColor=f6f6f6&color=9cf&style=flat&label=citations"></a>).
 -->
# 📖 Educations
- *2022.09 - Present*, PhD in Electronics and Computer Engineering, Hong Kong University of Science and Technology.
- *2018.08 - 2022.06*, BEng in Microelectronics Science and Engineering, School of Microelectronics, Southern University of Science and Technology. **GPA: 3.84/4.00, Rank: 4/93**
- *2015.09 - 2018.06*, [Guangdong Beijiang Middle School](https://zh.m.wikipedia.org/zh-hk/%E5%B9%BF%E4%B8%9C%E5%8C%97%E6%B1%9F%E4%B8%AD%E5%AD%A6).  

# 🎖 Honors and Awards
- *2024* HKUST RedBird Academic Excellence Award
- *2022* Hong Kong PhD Fellowship (HKPFS) 
- *2022* HKUST RedBird PhD Scholarship
- *2022* Outstanding Graduate (Top 8 in the College of Engineering, SUSTech) 
- *2021* China National Scholarship (Top 8 in SUSTech)
- *2021* Scientific Research Star (Top 1 in Shuren College, SUSTech)
- *2020* The First Prize of Outstanding Students in SUSTech (Top 5% in SUSTech)
- *2019* The Second Prize of Outstanding Students in SUSTech (Top 10% in SUSTech)

# 🔥 News
- *2022.6.6*: &nbsp;🎉🎉 Our stereo depth coprocessor has sucessfully been taped out in TSMC 28nm CMOS technology! 
- *2023.5.24*: &nbsp;🎉🎉 One paper "A 1920×1080 129fps 4.3pJ/Pixel Stereo-Matching Processor for Pico Aerial Vehicles" has been accepted by IEEE ESSDERC/ESSCIRC 2023!
- *2024.2.8*: &nbsp;🎉🎉 One collaborative paper "Stereo Matching Accelerator with Re-Computation Scheme and Data-Reused Pipeline for Autonomous Vehicles" has been accepted by IEEE Transactions on Circuits and Systems I: Regular Papers!
- *2024.2.27*: &nbsp;🎉🎉 One paper "Genetic Quantization-Aware Approximation for Non-Linear Operations in Transformers" has been accepted by ACM/IEEE Design Automation Conference (DAC) 2024! **(Acceptance Rate: 23%)**
- *2024.2.27*: &nbsp;🎉🎉 One paper "Additive Partial Sum Quantization" has been accepted by ACM/IEEE Design Automation Conference (DAC) 2024 Work-in-Progress Poster Session!
- *2024.5.9*: &nbsp;🎉🎉 I pass the PhD Qualifying Exam (PQE) and become a PhD candidate! 
- *2024.10.11*: &nbsp;🎉🎉 One paper "A 28nm 0.22μJ/Token Memory-Compute-Intensity-Aware CNN-Transformer Accelerator with Hybrid-Attention-Based Layer-Fusion and Cascaded Pruning for Semantic-Segmentation" has been accepted by IEEE International Solid-State Circuits Conference (ISSCC), 2025!

# 📝 Main Publications 

<div class='paper-box'><div class='paper-box-image'><div><img src='images/2024_ISSCC_v2.png' alt="sym" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

A 28nm 0.22μJ/Token Memory-Compute-Intensity-Aware CNN-Transformer Accelerator with Hybrid-Attention-Based Layer-Fusion and Cascaded Pruning for Semantic-Segmentation

**Pingcheng Dong**, Yonghao Tan, Xuejiao Liu, Peng Luo, Yu Liu, Luhong Liang, Yitong Zhou, Di Pang, Manto Yung, Dong Zhang, Xijie Huang, Shih-Yang Liu, Yongkun Wu, Fengshi Tian, Chi-Ying Tsui, Fengbin Tu, Kwang-Ting Cheng.

**2025**, *IEEE International Solid-State Circuits Conference (ISSCC)*

</div>
</div>


<div class='paper-box'><div class='paper-box-image'><div><img src='images/DAC_GQA.png' alt="sym" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

Genetic Quantization-Aware Approximation for Non-Linear Operations in Transformers

**Pingcheng Dong**, Yonghao Tan, Dong Zhang, Tianwei Ni, Xuejiao Liu, Yu Liu, Peng Luo, Luhong Liang, Shih-Yang Liu, Xijie Huang, Huaiyu Zhu, Yun Pan, Fengwei An and Kwang-Ting Cheng.

**2024**, *61th ACM/IEEE Design Automation Conference (DAC)*

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

**Pingcheng Dong**, Zhuoyu Chen, Zhuoao Li, Yuzhe Fu, Lei Chen, Fengwei An.  

**2021**, *IEEE Transactions on Circuits and Systems I: Regular Papers*

</div>
</div>


- [Configurable Image Rectification and Disparity Refinement for Stereo Vision](https://ieeexplore.ieee.org/abstract/document/9832005). **Pingcheng Dong**, Zhuoyu Chen, Zhuoao Li, Ruoheng Yao, Wenyue Zhang, Yangyi Zhang, Lei Chen, Chao Wang, Fengwei An. **2022** *IEEE Transactions on Circuits and Systems II: Express Briefs (TCAS-II)*


- [A 139 fps pixel-level pipelined binocular stereo vision accelerator with region-optimized semi-global matching](https://ieeexplore.ieee.org/abstract/document/9634805). **Pingcheng Dong**, Zhuoao Li, Zhuoyu Chen, Ruoheng Yao, Huanshihong Deng, Wenyue Zhang, Yangyi Zhang, Lei Chen, Chao Wang, Fengwei An. **2021** *IEEE Asian Solid-State Circuits Conference (A-SSCC)*

- [Real-Time FPGA-Based Binocular Stereo Vision System with Semi-Global Matching Algorithm](https://ieeexplore.ieee.org/abstract/document/9739626). Zhuoyu Chen, **Pingchen Dong**, Zhuoao Li, Ruoheng Yao, Yunhao Ma, Xiwei Fang, Huanshihong Deng, Wenyue Zhang, Lei Chen, Fengwei An. **2021** *IEEE 34th International System-on-Chip Conference (SOCC)*

- [Robot navigation based on pseudo-binocular stereo vision and linear fitting](https://ieeexplore.ieee.org/abstract/document/9332014). Huanshihong Deng, **Pingcheng Dong**, Zhuoao Li, Haoran Lyu, Yangyi Zhang, Yiwei Luo, Fengwei An. **2020** *IEEE International Conference on Integrated Circuits, Technologies and Applications (ICTA)*

# 📝 Collaborative Publications
- [Stereo Matching Accelerator with Re-Computation Scheme and Data-Reused Pipeline for Autonomous Vehicles](https://ieeexplore.ieee.org/document/10449892). Ke Li, Xiwei Fang, Yunhao Ma, Wenyue Zhang, **Pingcheng Dong**, Zhuoyu Chen, Lei Chen, Fengwei An. **2024**, *IEEE Transactions on Circuits and Systems I: Regular Papers*

- [BREAD: Boundary and Relation Distillation for Semantic Segmentation](https://arxiv.org/abs/2401.13174). Dong Zhang, **Pingcheng Dong**, Xinting Hu, Long Chen, Kwang-Ting Cheng. **2024**, *arXiv*

- [LLM-FP4: 4-Bit Floating-Point Quantized Transformers](https://arxiv.org/abs/2310.16836). Shih-yang Liu, Zechun Liu, Xijie Huang, **Pingcheng Dong**, Kwang-Ting Cheng. **2023**, *EMNLP Main Conference*

- [A Compact Hardware Architecture for Bilateral Filter with the Combination of Approximate Computing and Look-up Table](https://ieeexplore.ieee.org/abstract/document/9733932). Ruoheng Yao, Lei Chen, **Pingcheng Dong**, Zhuoyu Chen, Fengwei An. **2022**, *IEEE Transactions on Circuits and Systems II: Express Briefs*

# 😀 Teaching Assistant
- ELEC3400 Introduction to Integrated Circuits and Systems (2023 Spring)
- ELEC4320 FPGA based Design: From Theory to Practice (2023 Fall)



  
  



