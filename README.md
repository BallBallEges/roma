<div align="center">
  <h2>ROMA: A Role-Playing Multi-Agent Framework for Few-Shot Emotion-Cause Pair Extraction in Conversations</h2>
</div>


## About our Work
Emotion-cause pair extraction in conversations (ECPEC), which aims to jointly identify emotion utterances and their corresponding cause utterances in multi-party conversations, has garnered increasing interest. This task becomes particularly formidable under data-scarce conditions. Although large language models (LLMs) have achieved impressive performance on some Natural Language Processing (NLP) tasks, their capacity for handling few-shot ECPEC, which is characterized by complex causal relationships, remains largely unexplored. To fill this gap, we propose ROMA, a novel multi-agent framework with a systematic reasoning design, which provides the first systematic solution for few-shot ECPEC. ROMA employs LLM-based agents in a role-playing setting, engaging them in multi-round analysis and collaborative discussion, thereby enhancing LLMs’ persona understanding and causal reasoning capabilities. Specifically, our training-free framework comprises six critical stages: role construction, role and context enhancement, subjective emotion extraction, emotion self-reflection, dual-perspective cause extraction, and collaborative consultation for final decision-making. Our approach concentrates on the few-shot setting, which incurs lower annotation costs and better aligns with real-world scenarios. Experimental results on the ECPEC benchmark confirm that our method surpasses all baseline methods.

## Datasets
The ECF dataset files used in our experiments are provided in the `data/` directory. For more details about this dataset, please refer to the paper.
