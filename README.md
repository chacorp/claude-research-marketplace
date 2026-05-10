# Sihun's Claude Research Marketplace

개인 Claude Code 플러그인 마켓플레이스입니다.

## 설치 방법

```bash
/plugin marketplace add chacorp/claude-research-marketplace
```

## 플러그인 목록

### `hello-world`
예시 스킬 플러그인입니다.

| 스킬 | 설명 |
|------|------|
| `hello-world` | 이름을 받아 친근하게 인사합니다. |

### `research-helper`
구현 계획 수립부터 테스트 검증까지 자동화하는 플러그인입니다.

| 스킬 | 설명 |
|------|------|
| `implement` | 요청을 요약하고 구현 계획·검증 계획을 설계해 승인 후 구현 및 테스트 검증 루프를 수행합니다. 검증은 subagent가 테스트 코드로 진행하며, 최대 N회 루프 후 통과해야 완료 처리됩니다. |

## 플러그인 설치 방법

**1. 마켓플레이스 등록**

```bash
/plugin marketplace add chacorp/claude-research-marketplace
```

**2. 플러그인 설치**

```bash
/plugin install hello-world@sihun-marketplace
/plugin install research-helper@sihun-marketplace
```

**3. 스킬 사용**

```bash
# hello-world 플러그인
/hello-world:hello-world 이름

# research-helper 플러그인
/research-helper:implement 구현할 내용
```

## 새 플러그인 추가하기

1. `plugins/` 아래에 폴더 생성
2. `.claude-plugin/plugin.json` 작성 (매니페스트)
3. `skills/<스킬명>/SKILL.md` 작성 (스킬 정의)
4. `.claude-plugin/marketplace.json`의 `plugins` 배열에 항목 추가

### SKILL.md 기본 형식

```markdown
---
description: 스킬 설명 (Claude가 자동 호출 시 참고)
---

스킬 지시사항. $ARGUMENTS로 사용자 입력을 받습니다.
```
