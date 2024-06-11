#  Multimodal Large Language Model(MLLM) Note

*This note was created for research projects related to the understanding of Chinese charts and diagrams, compiling currently available open-source Multimodal Large Language Models (MLLM).*

*If you have any suggestions or notice any missing models, please feel free to let <sub><sub><a href="#me"><img src="https://img.shields.io/badge/me-000000"></a></sub></sub> know, Thank you!*


## Supports Chinese Conversations

<span id='id_llavanext'></span>
- ### <b>LLaVa-Next</b>  <sub><img src="https://img.shields.io/badge/30 Jan 2024-005AB5"></sub>
    
    <sub><sub>
    [![Code License](https://img.shields.io/badge/LLaVa%20Next-blog-66B3FF.svg)](https://llava-vl.github.io/blog/2024-04-30-llava-next-video/) [![Data License](https://img.shields.io/badge/LLaVa%20Next-Demo-81C954.svg)](https://github.com/tatsu-lab/stanford_alpaca/blob/main/DATA_LICENSE)
    <a href="https://github.com/LLaVA-VL/LLaVA-NeXT"> <img src="https://img.shields.io/github/stars/LLaVA-VL/LLaVA-NeXT.svg"></a>
    </sub></sub>


    > <b>*Authors*</b> : Yuanhan Zhang, Bo Li, Haotian Liu, Yong Jae Lee, Liangke Gui, Di Fu, Jiashi Feng, Ziwei Liu, Chunyuan Li

    > <b>*Introduction*</b>   
    In today’s exploration, we delve into the performance of LLaVA-NeXT within the realm of video understanding tasks. We reveal that LLaVA-NeXT surprisingly has strong performance in understanding video content. The current version of LLaVA-NeXT for videos has several improvements:  
    - <b>Zero-shot video representation capabilities with AnyRes</b>: The AnyRes technique naturally represents a high-resolution image into multiple images that a pre-trained VIT is able to digest, and forms them into a concantenated sequence. This technique is naturally generalizable to represent videos (consisting of multiple frames), allowing the image-only-trained LLaVA-Next model to perform surprisingly well on video tasks. Notably, this is the first time that LMMs show strong zero-shot modality transfer ability.  
    - <b>Inference with length generalization improves on longer videos.</b> The linear scaling technique enables length generalization, allowing LLaVA-NeXT to effectively handle long-video beyond the limitation of the "max_token_length" of the LLM.  
    - <b>Strong video understanding ability.</b>  
        - (1) LLaVA-Next-Image, which combines the above two techniques, yields superior zero-shot performance than open-source LMMs tuned on videos.  
        - (2) LLaVA-Next-Video, further supervised fine-tuning (SFT) LLaVA-Next-Image on video data, achieves better video understanding capabilities compared to LLaVA-Next-Image.  
        - (3) LLaVA-Next-Video-DPO, which aligns the model response with AI feedback using direct preference optimization (DPO), showing significant performance boost.  
    - <b>Efficient deployment and inference with SGLang.</b> It allows 5x faster inference on video tasks, allowing more scalable serving such as million-level video re-captioning.

    <b>*Related Work*</b> : <sub><sub><a href="#id_llava"><img src="https://img.shields.io/badge/LLaVa-8E8E8E"></a></sub></sub>

<span id='id_varytoy'></span>
- ### <b>Vary-toy</b>     <sub><img src="https://img.shields.io/badge/23 Jan 2024-005AB5"></sub>

    <p align="center">
    <a href="https://arxiv.org/abs/2401.12503"><img src="https://img.shields.io/badge/Vary_toy-paper-66B3FF"></a>
    <a href="https://vary.xiaomy.net/"><img src="https://img.shields.io/badge/Vary toy-Demo-81C954
    "></a>
    <a href="https://github.com/Ucas-HaoranWei/Vary-toy"> <img src="https://img.shields.io/github/stars/Ucas-HaoranWei/Vary-toy.svg"></a>
    </p>

    > <b>*Authors*</b> : [Haoran Wei*](https://scholar.google.com/citations?user=J4naK0MAAAAJ&hl=en), Lingyu Kong*, Jinyue Chen, Liang Zhao, [Zheng Ge](https://joker316701882.github.io/), [En Yu](https://scholar.google.com.hk/citations?user=rWCQMNgAAAAJ&hl=zh-CN&oi=sra), [Jianjian Sun](https://scholar.google.com/citations?user=MVZrGkYAAAAJ&hl=en), Chunrui Han, [Xiangyu Zhang](https://scholar.google.com/citations?user=yuB-cfoAAAAJ&hl=en)

    > <b>*Introduction*</b>    
    In Vary-toy, we introduce an improved vision vocabulary, allowing the model to not only possess all features of Vary but also gather more generality.  
    Specifically, we replace negative samples of natural images with positive sample data driven by object detection in the procedure of generating vision vocabulary, more sufficiently utilizing the capacity of the vocabulary network and enabling it to efficiently encode visual information corresponding to natural objects.  
    For experiments, Vary-toy can achieve 65.6% ANLS on DocVQA, 59.1% accuracy on ChartQA, 88.1% accuracy on RefCOCO, and 29% on MMVet.   

    <sub><sub>
    [![Code License](https://img.shields.io/badge/Code%20License-Apache_2.0-BE77FF.svg)](https://github.com/tatsu-lab/stanford_alpaca/blob/main/LICENSE) [![Data License](https://img.shields.io/badge/Data%20License-CC%20By%20NC%204.0-E278A6.svg)](https://github.com/tatsu-lab/stanford_alpaca/blob/main/DATA_LICENSE)
    </sub></sub>

    <b>*Related Work*</b> : <sub><sub><a href="#id_vary"><img src="https://img.shields.io/badge/Vary-8E8E8E"></a></sub></sub>
        

<span id='id_llava'></span>
- ### <b>LLaVa</b>  <sub><img src="https://img.shields.io/badge/17 Apr 2023-005AB5"></sub>

    <p align="center">
    <a href="https://arxiv.org/abs/2304.08485"><img src="https://img.shields.io/badge/LLaVa-paper-66B3FF
    "></a>
    <a href="https://llava.hliu.cc/"><img src="https://img.shields.io/badge/LLaVa-Demo-81C954
    "></a>
    <a href="https://github.com/haotian-liu/LLaVA"> <img src="https://img.shields.io/github/stars/haotian-liu/LLaVA.svg"></a>
    </p>

    > <b>*Authors*</b> : [Haotian Liu](https://hliu.cc), [Chunyuan Li](https://chunyuan.li/), [Yuheng Li](https://yuheng-li.github.io/), [Yong Jae Lee](https://pages.cs.wisc.edu/~yongjaelee/)

    > <b>*Introduction*</b>   
    LLaVA: Large Language and Vision Assistant, an end-to-end trained large multimodal model that connects a vision encoder and LLM for general-purpose visual and language understanding.  
    Our early experiments show that LLaVA demonstrates impressive multimodel chat abilities, sometimes exhibiting the behaviors of multimodal GPT-4 on unseen images/instructions, and yields a 85.1% relative score compared with GPT-4 on a synthetic multimodal instruction-following dataset.  
    When fine-tuned on Science QA, the synergy of LLaVA and GPT-4 achieves a new state-of-the-art accuracy of 92.53%.

    <sub><sub>
    [![Code License](https://img.shields.io/badge/Code%20License-Apache_2.0-BE77FF.svg)](https://github.com/tatsu-lab/stanford_alpaca/blob/main/LICENSE)
    </sub></sub>

    <b>*Related Work*</b> : <sub><sub><a href="#id_llavanext"><img src="https://img.shields.io/badge/LLaVa_Next-8E8E8E"></a></sub></sub>



## Currently Does Not Support Chinese Conversations

<span id='id_chartllama'></span>
- ### <b>ChartLLama</b>  


<span id='id_mplugdocowl'></span>
- ### <b>mPLUG-DocOwl</b>  


<span id='id_llava'></span>
- ### <b>ChartAst</b>  


## ToDo

- [ ] ChartLLama

- [ ] mPLUG-DocOwl

- [ ] ChartAst

## Contact Information
<span id='me'></span>
### Marine Wu  <sub>[![linkedin](https://img.shields.io/badge/linkedin-in-blue.svg)](https://www.linkedin.com/in/marine-wu-738a6b1a5/)</sub>

<sub>[![Email](https://img.shields.io/badge/Email-✉️-BE77FF.svg)](#)</sub>  ai4wu01mp6@gmail.com