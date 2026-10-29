# Codex 실무 과제 대비 Skills

이 저장소는 프로젝트 파일 파악 → 요구사항 질문 → 기술 선택 → 계획 → 구현 검토 → 검증 → 문서화 → 제출 점검 → 설명 연습을 돕는 **지침 기반 Codex Skills** 모음입니다.

## 포함된 Skills

- `map-project`: 현재 프로젝트 파일과 실행 흐름 요약
- `ask-requirements`: 요구사항 문서 분석 및 현업 담당자 질문 도출
- `pick-stack`: 기존 환경을 존중하는 프레임워크·기술 선택
- `plan-work`: 최소 구현 범위와 단계별 계획 수립
- `review-logic`: 핵심 로직 추적, AI 변경 내용·설계 근거 검토
- `verify-tests`: 테스트 계획·실행·증거 정리
- `work-notes`: 계획 문서와 협업 기록 관리
- `check-submit`: 제출 전 파일·요구사항·검증 상태 점검
- `explain-work`: 실제 산출물 기반 예상 서술형 질문으로 설명 가능 여부 점검

## 설치 방법

이 저장소의 **루트 디렉터리 자체를** 작업 환경의 `.agents/skills` 경로에 clone하면 됩니다. 이 저장소에는 각 Skill 폴더가 루트에 직접 들어 있습니다.

```bash
git clone https://github.com/<YOUR-USER>/<YOUR-REPO>.git .agents/skills
```

위 명령은 `.agents/skills` 디렉터리가 아직 없을 때 사용하세요. 이미 있다면 먼저 내용을 확인하고, 안전하게 별도 디렉터리에 clone한 뒤 Skill 폴더만 복사하세요.

```bash
git clone https://github.com/<YOUR-USER>/<YOUR-REPO>.git /tmp/codex-exam-skills
mkdir -p .agents/skills
cp -R /tmp/codex-exam-skills/{map-project,ask-requirements,pick-stack,plan-work,review-logic,verify-tests,work-notes,check-submit,explain-work} .agents/skills/
```

Codex가 Skill을 표시하지 않으면 세션을 다시 시작하세요. 명시적으로는 `$map-project`, `$ask-requirements`처럼 호출할 수 있습니다. 호출 문법은 사용 중인 Codex 버전에 따라 다를 수 있으므로, 해당 환경의 Skill picker/도움말도 확인하세요.

## 시험 중 사용 전 확인

- 대회 안내와 감독관 지침이 이 저장소보다 우선합니다.
- 공개 저장소를 clone하거나 Skill을 사용하는 것이 허용되는지 시험 규칙을 확인하세요.
- 이 팩은 기본적으로 `SKILL.md` 지침만 포함하며, 자동 실행 스크립트·외부 모델 연결·MCP 설정·hooks를 포함하지 않습니다.
- Git push는 하지 마세요. 제출용 파일명과 위치는 과제 안내를 따르세요.
- Skill의 제안은 사실이 아닐 수 있습니다. 코드·파일·테스트 결과를 실제로 확인한 뒤에만 문서화하세요.
