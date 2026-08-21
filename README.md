# ROMA

**ROMA: A Role-Playing Multi-Agent Framework for Few-Shot Emotion-Cause Pair Extraction in Conversations**

Jiaxin Yu, Qingbo Song, Wenyuan Liu, Yongjun He, Bineng Zhong

> **Paper status:** Under review  
> **Code status:** Full implementation and prompts will be released upon acceptance.

## Overview

ROMA is a training-free role-playing multi-agent framework for few-shot emotion-cause pair extraction in conversations (ECPEC). It organizes LLM-based agents around conversation participants and performs structured reasoning through six stages:

1. Role Construction
2. Role and Context Enhancement
3. Subjective Emotion Extraction
4. Emotion Self-Reflection
5. Dual-Perspective Cause Extraction
6. Collaborative Consultation

ROMA combines role-specific reasoning, self-reflection, experiencer/causer perspectives, and multi-round consultation to identify complex emotion-cause relationships in multi-party conversations.

## Highlights

- First LLM-based multi-agent framework for ECPEC.
- Training-free few-shot learning with role-playing agents.
- Dual-perspective cause extraction and collaborative consultation for complex causal reasoning.
- The 4-shot setting achieves an emotion-cause pair F1 score of **56.17%** on ECF.

## Repository

```text
roma/
├── data/
│   ├── README.md
│   ├── train.txt
│   └── test.txt
└── README.md
```

The repository currently provides the data used in the experiments. The complete implementation will be added after acceptance.

## Dataset

Experiments are conducted on the **ECF** benchmark for emotion-cause pair extraction in conversations. ECF contains 1,374 multi-party conversations, including 1,001 training conversations, 112 validation conversations, and 261 test conversations.

ROMA is training-free. The training split is used only as the source pool for selecting in-context demonstrations, while evaluation is conducted on the test split.

See [`data/README.md`](data/README.md) for data details and format.

## Main Configuration

| Setting | Value |
| --- | --- |
| Backbone LLM | GPT-OSS-120B |
| Temperature | 0 |
| Few-shot setting | 4-shot |
| Demonstration encoder | `all-mpnet-base-v2` |
| Demonstration selection | K-medoids |
| Maximum consultation rounds | 3 |
| Hardware | NVIDIA A100 80GB |

## Code Release

The complete ROMA implementation, prompts, demonstration-selection code, evaluation scripts, and experiment configurations will be released in this repository upon acceptance of the paper.

Planned release:

- [x] ECF data files
- [ ] ROMA implementation
- [ ] Prompts for all six stages
- [ ] Demonstration selection
- [ ] Evaluation scripts
- [ ] Reproduction scripts

## Citation

Citation information will be added after publication.

## Acknowledgments

This work was supported in part by the National Natural Science Foundation of China under Grants 62472109, 62473111, and 62576302.
