<div align="right">

**English** · [한국어](#한국어)

</div>

# LLM from Scratch — Study Notes

My notes and code from building a GPT-style language model step by step, from the tokenizer up to fine-tuning.
I am an embedded and test systems engineer moving into manufacturing AI; this repo is where I learn how LLMs work inside,
while my applied project [test-rig-anomaly-agent](https://github.com/sjpark513/test-rig-anomaly-agent) uses them in practice.

## Progress

| # | Topic | What I build | Status |
| --- | --- | --- | --- |
| 01 | [Tokenizer](01-tokenizer/) | Text → token IDs, byte-pair encoding | ⬜ |
| 02 | [Embeddings](02-embeddings/) | Token and position embeddings | ⬜ |
| 03 | [Attention](03-attention/) | Self-attention, causal mask, multi-head attention | ⬜ |
| 04 | [Transformer block](04-transformer-block/) | Layer norm, feed-forward, residual connections | ⬜ |
| 05 | [GPT model](05-gpt-model/) | Full model and text generation | ⬜ |
| 06 | [Pretraining](06-pretraining/) | Training loop, loss, loading pretrained weights | ⬜ |
| 07 | [Fine-tuning](07-finetuning/) | Classification and instruction fine-tuning | ⬜ |

⬜ not started · 🟨 in progress · ✅ done

Each folder holds a `NOTES.md` (what I learned, in my own words) and the code I wrote while following along.
The [log](log/) has a short entry for every study session.

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

토크나이저부터 파인튜닝까지 GPT 방식의 언어 모델을 한 단계씩 직접 만들어 보며 정리하는 공간입니다.
LLM이 안에서 어떻게 동작하는지를 여기서 배우고, 실제 활용은 [test-rig-anomaly-agent](https://github.com/sjpark513/test-rig-anomaly-agent)에서 합니다.

- 주제별 폴더마다 `NOTES.md`(내 말로 정리한 내용)와 강의를 따라 직접 작성한 코드를 둡니다.
- 공부한 날마다 [log](log/)에 짧은 기록을 남깁니다.
- 진행 상황은 위 Progress 표에서 관리합니다.
