### 측정을 먼저 고정합니다

저장소 넷이 결국 같은 얘기를 합니다. 결과를 내기 전에, 그 결과가 맞는지 잴 방법을 먼저 만든다.

[agent-workflow](https://github.com/serenwoon/agent-workflow)는 문서 작업을 에이전트로 돌리는 판정 루프입니다. 규칙이 여덟 개 있는데 미리 설계한 건 하나도 없어요. 전부 뭔가를 틀린 다음에 생겼습니다. 그중 다섯은 같은 실패였고요. 도구가 준 결과를 원본과 안 맞춰보고 그냥 받은 것.

[extraction-benchmark](https://github.com/serenwoon/extraction-benchmark)에서는 같은 작업을 사람과 파이프라인으로 나눠 쟀습니다. 건당 60초가 8.6초가 됐습니다. 그런데 본문을 뒤집는 단서는 양쪽 다 놓쳤어요. 사람이 0/4, LLM이 0~1/4, 기계 스캔만 4/4였습니다.

[requirement-guard](https://github.com/serenwoon/requirement-guard)는 제안서 원고를 규격 문서 원본과 대조합니다. 재활용한 문장에 앞 사업의 요구사항 ID와 이름이 딸려 오는 걸 잡으려고 만들었어요. 정작 만들고 보니 ID가 아예 없는 경우는 0건이더군요. 사고는 ID가 멀쩡하고 이름만 다른 쪽이었습니다.

공백 뒤를 전부 이름으로 보면 후보 84건에 진짜는 2건, 정밀도 2%짜리가 나옵니다. 신호를 둘로 좁혀 243건 중 2건, 오탐 0으로 만들었습니다.

그 2건도 정직하게 말하면 이미 고쳐서 「고쳐야 할 것」 표에 적어둔 기록이었습니다. 살아 있는 오류는 0건이었어요. 검사기가 진짜 발화하는지는 저 숫자가 아니라 골든셋이 증명합니다.

[youtube-sentiment-pipeline](https://github.com/serenwoon/youtube-sentiment-pipeline)은 댓글 감정 3분류입니다. 어떤 방법도 무작위 추측을 못 넘었습니다. 골든셋 198건으로는 그 차이를 잴 수 없다, 거기까지가 결과입니다.

뒤의 둘을 봐주세요. 좋은 결과가 아니라, 좋은 결과를 얻었다고 착각하지 않는 방법이 거기 있습니다.

---

하나만 읽으신다면 [agent-workflow README 4절](https://github.com/serenwoon/agent-workflow#4-실패에서-나온-규칙)입니다. 실패 여덟 건과 거기서 나온 규칙.
