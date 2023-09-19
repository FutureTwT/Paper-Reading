# 参数高效的迁移

## 2022.10

(EMNLP) **Parameter-Efficient Tuning Makes a Good Classification Head** [[Paper]](https://aclanthology.org/2022.emnlp-main.514.pdf)

  - 汇总了常见的模型迁移策略：Fully-FT对backbone和clf head全部调整；Linear-Probe只针对clf head；LP-FT是先经过Linear probe对clf head预热，然后进行Fully-FT；本文提出了EH-FT，并从本质上探究了各类微调细节带来的影响
  - 对backbone部分参数调整叫做parameter-efficient tuning，常见机制如LoRA，Prefix-Tuning等
  - 原理大概就是在第一阶段对backbone和clf head执行parameter-efficient tuning，然后恢复backbone参数，保留clf更新后参数，在第二阶段进行Fully-FT


