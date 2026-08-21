# ROMA

Official repository for the manuscript **“ROMA: A Role-Playing Multi-Agent Framework for Few-Shot Emotion-Cause Pair Extraction in Conversations.”**

> **Status:** The manuscript is currently under review. The complete source code, prompts, and reproduction scripts will be released upon acceptance.

## Overview

Emotion-cause pair extraction in conversations (ECPEC) aims to jointly identify emotion utterances and their corresponding cause utterances in multi-party conversations. ROMA is a training-free, role-playing multi-agent framework designed for few-shot ECPEC. It instantiates role-playing agents for conversation participants and performs systematic reasoning through six stages:

1. Role Construction
2. Role and Context Enhancement
3. Subjective Emotion Extraction
4. Emotion Self-Reflection
5. Dual-Perspective Cause Extraction
6. Collaborative Consultation

The framework combines role-specific reasoning, self-reflection, dual-perspective cause extraction, and multi-round agent consultation to identify complex emotion-cause relationships under few-shot settings.

## Repository Status

This repository currently provides the data files used in our experiments. The implementation is being prepared for public release.

After the paper is accepted, this repository will be updated with:

- the complete ROMA implementation;
- prompts for all reasoning stages;
- demonstration-selection code;
- evaluation scripts;
- configurations for the backbone LLMs;
- scripts for reproducing the main results, ablation studies, and additional analyses.

## Data

Experiments are conducted on the **ECF benchmark dataset** for emotion-cause pair extraction in conversations. ECF is built upon MELD and augments conversations with cause annotations for six non-neutral emotion categories: anger, disgust, fear, joy, sadness, and surprise.

The dataset contains 1,374 multi-party conversations, including 1,001 training conversations, 112 validation conversations, and 261 test conversations. In ROMA, the framework is training-free: demonstrations are selected from the training data, while evaluation is conducted on the test set.

The data files included in this repository are located in `data/`:

```text
data/
├── train.txt
├── test.txt
└── README.md
```

Please see [`data/README.md`](data/README.md) for details.

## Experimental Configuration

The main experiments use the following setup:

- **Backbone LLM:** GPT-OSS-120B
- **Generation temperature:** 0
- **Maximum consultation rounds:** 3
- **Sentence encoder for demonstration selection:** `all-mpnet-base-v2`
- **Demonstration selection:** K-medoids clustering
- **Default few-shot setting:** 4-shot
- **Hardware:** one NVIDIA A100 GPU (80 GB)

## Code Release

The manuscript is currently under review. To avoid inconsistencies between the submitted manuscript and an evolving implementation, the source code is not yet publicly released.

**The complete code and prompts will be released in this repository upon acceptance of the paper.**

## Citation

Citation information will be added after publication.

## Acknowledgments

This work was supported in part by the National Natural Science Foundation of China under Grants 62472109, 62473111, and 62576302.

## Contact

For questions about the paper or repository, please open an issue after the public code release.
