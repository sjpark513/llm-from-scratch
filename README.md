<div align="right">

**English** · [한국어](#한국어)

</div>

# LLM from Scratch — Study Notes

My notes and code from building language models step by step: from counting N-grams, through a neural language model and the Transformer, to pretraining and fine-tuning a chat model.
I follow HongLab's course series *LLM 바닥부터 만들기* ([course page](https://www.honglab.ai/courses/llmpt1)) and write everything here in my own words.
I am an embedded and test systems engineer moving into manufacturing AI; this repo is where I learn how LLMs work inside,
while my applied project [test-rig-anomaly-agent](https://github.com/sjpark513/test-rig-anomaly-agent) uses them in practice.

## Progress

| Part | Chapter | What I build | Status |
| --- | --- | --- | --- |
| 1. Statistical LMs | [Ch.1 Warm-up](part1-statistical-lm/ch01-warmup/) | How AI agents work; setting up a coding agent | ⬜ |
| | [Ch.2 N-grams](part1-statistical-lm/ch02-ngram/) | Character statistics, bigram/trigram/N-gram models, sentence generation, Korean morphological analysis | ⬜ |
| 2. Neural LMs | [Ch.3 Neural LMs](part2-neural-lm/ch03-neural-lm/) | Limits of N-grams, perplexity, word embeddings | ⬜ |
| | [Ch.4 Neural networks](part2-neural-lm/ch04-neural-network/) | NPLM trained on Korean Wikipedia, CPU optimization | ⬜ |
| 3. Transformer & pretraining | [Ch.5 Transformer](part3-transformer-pretraining/ch05-transformer/) | Transformer architecture and modern recipes | ⬜ |
| | [Ch.6 Pretraining](part3-transformer-pretraining/ch06-pretraining/) | PyTorch implementation, scaling up on cloud GPUs, in-context learning | ⬜ |
| 4. Conversational AI | [Ch.7 Fine-tuning](part4-conversational-ai/ch07-finetuning/) | Training pipeline, instruction tuning, full fine-tuning | ⬜ |
| | [Ch.8 Persona](part4-conversational-ai/ch08-persona/) | Persona tuning, synthetic data, open models, PEFT | ⬜ |

⬜ not started · 🟨 in progress · ✅ done

Each chapter folder holds a `NOTES.md` (lesson checklist and what I learned) and the code I wrote while following along.
The [log](log/) has a short entry for every study session.

## Notes on course material

Lecture videos, slides and the instructor's code are not copied here. This repo contains only my own summaries and the code I wrote myself (with an AI coding agent, as the course recommends).

## Setup

```bash
python -m venv .venv && source .venv/bin/activate   # Windows: .venv\Scripts\activate
pip install -r requirements.txt
```

---

<a id="한국어"></a>

<div align="right">

[English](#llm-from-scratch--study-notes) · **한국어**

</div>

# LLM 바닥부터 만들기 — 학습 기록

홍정모 연구소(HongLab)의 [LLM 바닥부터 만들기](https://www.honglab.ai/courses/llmpt1) 강의를 따라, 앤그램 통계부터 뉴럴 언어 모델, 트랜스포머, 사전학습, 대화형 AI 파인튜닝까지 직접 만들어 보며 정리하는 공간입니다.
LLM이 안에서 어떻게 동작하는지를 여기서 배우고, 실제 활용은 [test-rig-anomaly-agent](https://github.com/sjpark513/test-rig-anomaly-agent)에서 합니다.

- 파트(1~4)와 챕터(1~8)는 강의 구성을 그대로 따릅니다.
- 챕터 폴더마다 `NOTES.md`(강의 체크리스트와 내 말로 정리한 내용)와 직접 작성한 코드를 둡니다.
- 공부한 날마다 [log](log/)에 짧은 기록을 남깁니다.
- 강의 영상·슬라이드·강사 코드는 올리지 않고, 내가 정리한 내용과 직접 짠 코드만 올립니다.
