적용 예시는 [여기](https://github.com/ktb-23/collaboration-document/blob/main/example/commit-message-convention.md)서 확인 가능합니다

# 목표

커밋 히스토리 탐색 환경 구축

GitHub 및 다양한 git 도구에서 메시지를 가독성 향상

# 규칙

### 커밋 메시지 형식

```bash
<type>: <subject>
<BLANK LINE>
<description> (선택)
<BLANK LINE> (description 작성시)
<referencing issue number>
<BLANK LINE>
<breaking change> (선택)
```

- 각 줄은 100자를 넘지 않는다
- 예시와 같이 헤더, 본문, 풋터로 구성하며 각 섹션은 빈 줄로 구분

<br/>

### Revert

커밋이 이전 커밋을 되돌리는 경우에 한해 기존 규칙에 다음 규칙을 추가

- 헤더에 `revert:` 추가
- 본문은 "This reverts commit <hash>"으로 시작 (`<hash>`는 되돌리는 커밋의 SHA)

<br/>

### 메시지 헤더 (type + subject)

메시지 헤더는 타입 및 주제를 포함하는 간결한 설명

#### type

아래 항목 중 상황에 맞게 선택

- feat (기능 추가)
- fix (버그 수정)
- docs (문서 작업)
- style (디자인 수정)
- refactor (리팩토링)
- test (테스트 추가)
- build (빌드)
- chore (잡일)

#### subject

변경에 대한 매우 짧은 설명입니다.

- 문법적으로 좋은 문장을 작성하는것보다 가독성에 초점
- 예: 끝에 마침표(.) 사용하지 않기 등

<br/>

### 메시지 본문

#### description (선택)

- <subject>와 동일하게 문법적으로 좋은 문장을 작성하는것보다 가독성에 초점
- 변경 및 수정 사항의 경우 변경 사유 및 변경 사항 작성

#### referencing issue number (필수)

예시) #123, #245, #992

<br/>

### 메시지 풋터 (선택)

#### breaking change - 호환성

동일한 기능이 이전과 호환이 되지 않는 경우 작성

"BREAKING CHANGE:"라는 단어로 시작하며 변경 설명, 정당성 및 마이그레이션 노트 작성
