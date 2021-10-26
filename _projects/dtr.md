---
title: Dynamic Tensor Rematerialization

description: |
  Checkpointing deep learning models as a dynamic analysis

people:
  - kirisame
  - sslyu
  - altanh
  - jrb
  - mikehe
  - jroesch
  - tqchen
  - ztatlock

layout: project
last-updated: 2021-10-25
---

See our [ICLR '21 paper](https://arxiv.org/abs/2006.09616) and [talk](https://www.youtube.com/watch?v=S9KJ37Sx2XY). Our prototype implementation can be found [here](https://github.com/uwsampl/dtr-prototype).

Dynamic Tensor Rematerialization (DTR) allows for training deep learning models in less memory by using a heuristic to evict tensors from memory once there is not enough memory for an allocation and recomputing them on demand, acting as a tensor-level cache. Despite the simplicity of its approach, DTR can allow for training larger models in the same amount of memory with only modest amounts of overhead. We hope to apply our technique to further settings for deep learning applications as well as to other domains.

DTR has been adopted by the [MegEngine framework](https://github.com/MegEngine/MegEngine/wiki/Reduce-GPU-memory-usage-by-Dynamic-Tensor-Rematerialization).
