# Sihun's Claude Research Marketplace

개인 Claude Code 플러그인 마켓플레이스입니다.

## 설치 방법

```bash
/plugin marketplace add sihun-cha/claude-research-marketplace
```

## 플러그인 목록

| 이름 | 설명 |
|------|------|
| `hello-world` | 예시 스킬 플러그인 |

## 플러그인 사용법

마켓플레이스 추가 후:

```bash
/plugin install hello-world@sihun-marketplace
```

설치 후 스킬 사용:
```bash
/hello-world:hello-world 이름
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
