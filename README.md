# knowhow-script — 후킹 + 노하우텔링 스크립트 스킬

내 경험에서 나온 방법(노하우)을 **첫 1~2초 후킹 멘트**와 합쳐 45~60초 릴스·쇼츠 스크립트 초안으로 만들어 주는 Claude 스킬입니다.

> 정보만 주면 누구나 쓸 수 있는 글이 되고, 이야기만 하면 남는 게 없습니다.
> 노하우텔링은 "내가 해보니 이랬다"를 뼈대로, 그 과정에서 얻은 방법을 줍니다.

## 무엇을 해 주나요

1. **경험 재료 인터뷰** — 질문 6개로 언제·무엇을 잃었고·무엇을 알게 됐는지 모읍니다
2. **노하우 한 줄** — 시청자가 따라 할 방법을 먼저 정합니다
3. **후킹 6안** — 의도 10분류에서 3개를 골라 단정·질문·공감 톤으로. 15자 컷 버전 + 바로 뒤 1~3문장(락인 존)까지
4. **5단계 대본** — 후킹 → 서사 → 문제 발생 → 과정 → 해결
5. **장면표** — 문장마다 화면 지시와 제작 방식
6. **규칙 검사** — 없는 숫자·과장·지어낸 경험을 걸러냅니다

이미 쓴 대본을 주면 첫머리에서 이탈하는 지점을 진단하고 고친 안을 냅니다.

## 설치

### Claude Code (명령 두 줄)
```
/plugin marketplace add wiiskey/knowhow-script
/plugin install knowhow-script@knowhow-script
```

### Claude Code (직접 복사)
```bash
git clone https://github.com/wiiskey/knowhow-script.git
cp -r knowhow-script/skills/knowhow-script ~/.claude/skills/
```

### Claude.ai 웹·데스크톱 앱
1. [Releases](../../releases)에서 `knowhow-script.zip` 다운로드
2. 설정 → 기능(Capabilities) → 스킬 → 스킬 업로드 → zip 선택

## 사용 예시

```
노하우텔링 스크립트 써줘. 키 158인데 바지 핏 맞추느라 3년 동안 반품만 하다가 찾은 방법
```
```
내 경험으로 대본 만들어줘 — 파운데이션 10개 실패하고 턱선 테스트로 고르게 된 얘기, 45초
```
```
이 대본 첫머리 진단해줘: (대본 붙여넣기)
```

결과물은 현재 폴더의 `knowhow-scripts/날짜-소재.md`로 저장됩니다.

## 나만의 스킬로 키우기 (선택)

작업 폴더에 아래 파일을 두면 스킬이 우선 적용합니다.

| 파일 | 넣을 내용 |
|---|---|
| `my-voice.md` | 내 말투 — 자주 쓰는 어미, 안 쓰는 말, 예시 문장 3~5개 |
| `brand-rules.md` | 금지어 목록 · 써도 되는 숫자·증거(실제 후기 수, 판매량 등) |

## 파일 구조

```
skills/knowhow-script/
├── SKILL.md                     # 7단계 워크플로우
└── references/
    ├── hook-intents.md          # 후킹 의도 10분류 · 빈칸 패턴 · 노하우텔링 변환
    ├── rules.md                 # 검사 규칙 G1~G8 · 의도 결정표 · 락인 존 · 진단
    └── output-template.md       # 결과물 양식
```

## 라이선스
MIT
