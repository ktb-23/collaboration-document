# 브랜치 전략 & 병합 규칙

우리 팀은 다음에 따라 브랜치 생성, 관리, 병합을 진행합니다.

## 브랜치 생성, 관리 규칙

GitHub Flow를 기반으로 가감된 규칙입니다.

## 1. Main 브랜치
- `main` 브랜치는 항상 배포 가능한 상태를 유지합니다.
- `main` 브랜치에 직접 커밋하지 않고, `dev` 브랜치를 통해서만 병합합니다.

## 2. Dev 브랜치
- `dev` 브랜치는 테스트 환경을 위한 브랜치 입니다.
- `dev` 모든 테스트가 종료된 후 main 브랜치에 병합을 진행합니다.
- `dev` 브랜치에 직접 커밋하지 않으며 모든 변경 사항은 feature 브랜치를 통해 처리합니다.

## 3. Feature 브랜치 생성
- 새로운 기능, 버그 수정, 실험적인 코드를 개발할 때마다 `dev` 브랜치에서 새로운 브랜치를 생성합니다.
- 브랜치 이름은 작업 내용을 명확히 설명해야 합니다.
  - 예시: `add-user-authentication`, `fix-login-bug`

## 4. 커밋 및 푸시
- 기능 개발이나 수정 작업을 진행하면서 주기적으로 커밋합니다.
- 작업이 완료되면 로컬 브랜치를 GitHub 리포지토리로 푸시합니다.
- 커밋 메시지는 명확하고 간결하게 작성합니다.
- 보다 자세한 내용은 [여기](https://github.com/ktb-23/collaboration-document/blob/main/commit-message-convention.md)서 확인 가능합니다.

## 5. 코드 리뷰 및 피드백
- PR이 생성되면 팀원들이 리뷰를 진행합니다.
- 리뷰어는 코드를 검토하고 개선 사항이나 추가 작업이 필요한 부분에 대해 피드백을 제공합니다.
- 리뷰 과정에서 발견된 문제를 수정하고, 추가 커밋을 통해 PR을 업데이트합니다.
- 보다 자세한 내용은 [여기](https://github.com/ktb-23/collaboration-document/blob/main/code-review.md)서 확인 가능합니다.

## 6. 브랜치 정리
- 작업이 완료된 feature 브랜치는 `main`에 병합된 후 삭제하여 깔끔한 브랜치 구조를 유지합니다.

## 병합 규칙

1. **Main Branch로의 병합**
   - Main으로의 모든 병합은 반드시 Dev 브랜치 내용을 포함한 PR을 통해서만 가능합니다.

2. **Dev Branch로의 병합**
   - Dev로의 모든 병합은 반드시 PR을 통해 이루어져야 합니다.

3. **Pull Request (PR) Approvals**
   - Main과 Dev 브랜치에 병합하기 위해서는 페어 파트너의 Approve가 필요합니다.
   - 코멘트나 피드백에 따른 수정이 완료된 경우에만 Approve 합니다.
   - 새로운 commit이 PR에 추가된 경우 Approve가 취소됩니다.

4. **Conversation Resolution**
   - PR 내 모든 대화(conversation)는 종결되어야 합니다.

5. **Conflict Trouble Shooting**
   - Conflict 발생시 기존 코드를 우선으로 합니다.
   - 새로운 코드를 Merge하고싶은 경우 기존 코드를 작성한 사람과 논의를 진행합니다.
   - 해당 논의는 Discord > 요청 채널을 사용합니다.