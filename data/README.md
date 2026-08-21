# ECF Data

This directory contains the ECF data files used by ROMA.

## Dataset

The experiments in the paper use the **ECF benchmark dataset** introduced in:

> F. Wang, Z. Ding, R. Xia, Z. Li, and J. Yu, “Multimodal Emotion-Cause Pair Extraction in Conversations,” *IEEE Transactions on Affective Computing*, 14(3), 1832–1844, 2023. DOI: 10.1109/TAFFC.2022.3226559.

ECF is built upon the MELD dataset and augments multi-party conversations with emotion-cause annotations. The paper reports 1,374 conversations in total, with 1,001 training conversations, 112 validation conversations, and 261 test conversations.

## Files

- `train.txt`: training data used as the source pool for few-shot demonstration selection.
- `test.txt`: test data used for evaluation.

ROMA is training-free and does not optimize model parameters on the training set. Instead, the training data are used only to select in-context demonstrations. In the main setting, four demonstrations are selected through semantic embedding and K-medoids clustering.

## Data Format

Each conversation block contains conversation-level identifiers and annotated emotion-cause pairs, followed by utterances. An utterance record includes the utterance index, speaker, emotion label, utterance text, and source timestamp information.

The emotion-cause pair annotation `(i, j)` indicates that utterance `i` is the emotion utterance and utterance `j` is its corresponding cause utterance.

## Notes

These files are provided for reproducing the experiments reported in the ROMA paper. Please cite the original ECF paper when using the dataset.
