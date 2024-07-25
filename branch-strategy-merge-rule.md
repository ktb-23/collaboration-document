# Branch Strategy and Merge Rules

우리 팀은 GitHub Flow를 기준으로 다음과 같은 브랜치 전략과 머지 규칙을 따릅니다.

## Branch Strategy

1. **Main Branch**
   - 배포 가능한 코드만 포함합니다.
   - 안정적인 상태를 유지합니다.

2. **Dev Branch**
   - 통합 테스트와 검증을 위한 브랜치입니다.
   - 다양한 feature branches가 이곳에서 결합되어 검토됩니다.

3. **Feature Branches**
   - 새로운 기능, 수정사항 또는 실험을 위해 사용됩니다.
   - `feature/`, `bugfix/` 등으로 네이밍합니다.

## Merge Rules

1. **Main Branch로의 Merge**
   - Main으로의 모든 병합은 반드시 Dev 브랜치 내용을 포함한 PR을 통해서만 가능합니다.

2. **Dev Branch로의 Merge**
   - Dev로의 모든 병합은 반드시 PR을 통해 이루어져야 합니다.

3. **Pull Request (PR) Approvals**
   - Main과 Dev 브랜치에 병합하기 위해서는 페어 파트너의 Approve가 필요합니다.
   - 코멘트나 피드백에 따른 수정이 완료된 경우에만 Approve 합니다.

4. **Conversation Resolution**
   - PR 내 모든 대화(conversation)는 종결되어야 합니다.
