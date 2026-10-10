<div align="right">

**English** · [한국어](#한국어)

</div>

# LLM from Scratch — Study Notes

My notes and code from building language models step by step: from counting N-grams, through a neural language model and the Transformer, to pretraining and fine-tuning a chat model.
I follow HongLab's course series *LLM From Scratch* ([course page](https://www.honglab.ai/courses/llmpt1)) and write everything here in my own words.
I am an embedded and test systems engineer moving into manufacturing AI. This repo is where I learn how LLMs work inside,
while my applied project [test-rig-anomaly-agent](https://github.com/sjpark513/test-rig-anomaly-agent) uses them in practice.

## Progress

Part 1 completed in October 2026.

| Part | Chapter | What I build | Status |
| --- | --- | --- | --- |
| 1. Statistical LMs | [Ch.1 Warm-up](part1-statistical-lm/ch01-warmup/) | How AI agents work; setting up a coding agent | ✅ |
|  | [Ch.2 N-grams](part1-statistical-lm/ch02-ngram/) | Character statistics, bigram/trigram/N-gram models, sentence generation, Korean morphological analysis | ✅ |
| 2. Neural LMs | [Ch.3 Neural LMs](part2-neural-lm/ch03-neural-lm/) | Limits of N-grams, perplexity, word embeddings | ⬜ |
|  | [Ch.4 Neural networks](part2-neural-lm/ch04-neural-network/) | NPLM trained on Korean Wikipedia, CPU optimization | ⬜ |
| 3. Transformer & pretraining | [Ch.5 Transformer](part3-transformer-pretraining/ch05-transformer/) | Transformer architecture and modern recipes | ⬜ |
|  | [Ch.6 Pretraining](part3-transformer-pretraining/ch06-pretraining/) | PyTorch implementation, scaling up on cloud GPUs, in-context learning | ⬜ |
| 4. Conversational AI | [Ch.7 Fine-tuning](part4-conversational-ai/ch07-finetuning/) | Training pipeline, instruction tuning, full fine-tuning | ⬜ |
|  | [Ch.8 Persona](part4-conversational-ai/ch08-persona/) | Persona tuning, synthetic data, open models, PEFT | ⬜ |

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

앤그램 빈도 세기에서 시작해 뉴럴 언어 모델과 트랜스포머를 거쳐, 대화형 모델의 사전학습과 파인튜닝까지 언어 모델을 한 단계씩 직접 만들며 정리한 노트와 코드입니다.
홍랩(HongLab)의 강의 시리즈 「LLM 바닥부터 만들기」([강의 페이지](https://www.honglab.ai/courses/llmpt1))를 따라가며, 모든 내용을 제 말로 정리합니다.
저는 임베디드·시험 설비 엔지니어로서 제조 AI 분야로 전환하고 있습니다. 이 레포에서는 LLM이 안에서 어떻게 동작하는지를 배우고,
실제 활용은 [test-rig-anomaly-agent](https://github.com/sjpark513/test-rig-anomaly-agent) 프로젝트에서 합니다.

## 진행 상황

2026년 10월 파트 1 완료.

| 파트 | 챕터 | 만드는 것 | 상태 |
| --- | --- | --- | --- |
| 1. 통계적 언어 모델 | [챕터 1. 워밍업](part1-statistical-lm/ch01-warmup/) | AI 에이전트의 동작 원리, 코딩 에이전트 준비 | ✅ |
|  | [챕터 2. 앤그램](part1-statistical-lm/ch02-ngram/) | 문자 빈도 통계, 바이그램·트라이그램·앤그램 모델, 문장 생성, 한국어 형태소 분석 | ✅ |
| 2. 뉴럴 언어 모델 | [챕터 3. 뉴럴 언어 모델](part2-neural-lm/ch03-neural-lm/) | 앤그램의 한계, 퍼플렉시티, 워드 임베딩 | ⬜ |
|  | [챕터 4. 뉴럴 네트워크](part2-neural-lm/ch04-neural-network/) | 한국어 위키로 학습한 NPLM, CPU 최적화 | ⬜ |
| 3. 트랜스포머와 사전학습 | [챕터 5. 트랜스포머](part3-transformer-pretraining/ch05-transformer/) | 트랜스포머 구조와 현대적 레시피 | ⬜ |
|  | [챕터 6. 사전훈련](part3-transformer-pretraining/ch06-pretraining/) | 파이토치 구현, 클라우드 GPU 스케일업, 인컨텍스트 러닝 | ⬜ |
| 4. 대화형 AI | [챕터 7. 파인튜닝](part4-conversational-ai/ch07-finetuning/) | 훈련 파이프라인, 지시 튜닝, 전체 미세 조정 | ⬜ |
|  | [챕터 8. 페르소나](part4-conversational-ai/ch08-persona/) | 페르소나 튜닝, 합성 데이터, 공개 모델, PEFT | ⬜ |

⬜ 시작 전 · 🟨 진행 중 · ✅ 완료

챕터 폴더마다 `NOTES.md`(강의 체크리스트와 배운 내용)와 강의를 따라 직접 작성한 코드를 둡니다.
공부한 날마다 [log](log/)에 짧은 기록을 남깁니다.

## 강의 자료에 대해

강의 영상, 슬라이드, 강사의 코드는 이곳에 올리지 않습니다. 이 레포에는 제가 직접 정리한 내용과 직접 작성한 코드만 있습니다(강의 권장대로 AI 코딩 에이전트와 함께 작성).

## 실행 환경 준비

```bash
python -m venv .venv && source .venv/bin/activate   # Windows: .venv\Scripts\activate
pip install -r requirements.txt
```
