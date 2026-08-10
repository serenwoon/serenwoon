### 측정을 먼저 고정합니다

저장소 셋이 결국 같은 얘기를 합니다. **결과를 내기 전에, 그 결과가 맞는지 잴 방법을 먼저 만든다.**

| | |
|---|---|
| **[agent-workflow](https://github.com/serenwoon/agent-workflow)** | 문서 작업을 에이전트로 돌리는 판정 루프. 규칙이 여덟 개 있는데 미리 설계한 건 하나도 없습니다. 전부 뭔가를 틀린 다음에 생겼어요. 그중 다섯은 같은 실패였고요 — 도구가 준 결과를 원본과 안 맞춰보고 그냥 받은 것 |
| **[extraction-benchmark](https://github.com/serenwoon/extraction-benchmark)** | 같은 작업을 사람과 파이프라인으로 나눠 쟀습니다. 건당 60초 → 8.6초. 그런데 본문을 뒤집는 **단서는 양쪽 다 놓쳤습니다** (사람 0/4 · LLM 0~1/4 · 기계 스캔 4/4) |
| **[youtube-sentiment-pipeline](https://github.com/serenwoon/youtube-sentiment-pipeline)** | 댓글 감정 3분류. **어떤 방법도 무작위 추측을 못 넘었습니다.** 골든셋 198건으로는 그 차이를 잴 수 없다, 거기까지가 결과입니다 |

셋 중에 세 번째를 봐주세요. **좋은 분류기가 아니라, 좋은 분류기를 골랐다고 착각하지 않는 방법**이 거기 있습니다.

---

하나만 읽으신다면 → [agent-workflow README 4절](https://github.com/serenwoon/agent-workflow#4-실패에서-나온-규칙--이-문서의-본체) · 실패 여덟 건과 거기서 나온 규칙
