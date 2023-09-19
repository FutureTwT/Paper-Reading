# 大模型适配

## 2023.6

(Arxiv) **Adapting Pre-trained Language Models to Vision-Language Tasks via Dynamic Visual Prompting** [[Paper]](https://xianbai.me/learn-md/article/syntax/links.html)

  - 将PLM适配到下游的VL task中，在VL的输入基础上，将visual modality视作prompt，添加到text modality上，输入到PLM中
  - 直接在text sequence上拼接image sequence进行PLM适配效率太低，采用cross-modal MHA来实现text token对image token查询，使得密集的image token缩减至text sequence的长度
  - 进一步，对于encoder-only的PLM (Bert)，选择当前层的[CLS]特征来查询image token，将text方向的运算量降低；encoder-decoder的设计与其近似
  - 考虑到不同的VL task采用固定的Prompt插入技术，提出k-Armed Bandit (K-臂赌博机) based Automatic Prompt Placement，通过某种搜索策略来评估最优的插入位置


