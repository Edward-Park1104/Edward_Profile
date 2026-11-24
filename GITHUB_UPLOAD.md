# GitHub 업로드 안내

## 현재 상태

이 폴더에는 이미 Git 저장소와 기존 커밋이 있습니다. GitHub 저장소 주소는 아직 연결되지 않았습니다. 새로 Git을 초기화할 필요는 없습니다.

## 올리기 전 확인

1. GitHub에서 새 저장소를 만듭니다. 기존 커밋을 그대로 올릴 수 있도록 빈 저장소로 만드는 것이 편리합니다.
2. 공개 저장소로 만들 경우 `edward.md`, `README.md`, `AGENTS.md` 등 올릴 문서의 공개 범위를 확인합니다.
3. 터미널에서 프로젝트 폴더로 이동하고 변경 사항을 살펴봅니다.

   ```bash
   cd /Users/edwardpark/Documents/Codex/Vibe_example/Profile_GPT
   git status
   git diff
   ```

4. 포함할 변경 사항을 선택해 커밋합니다. 커밋된 기존 소스와 이미지는 이전 기록에 그대로 포함되어 있습니다. 환경 파일이나 비밀번호, 토큰은 추가하지 마세요.
5. GitHub에서 발급받은 저장소 주소를 사용해 원격 저장소를 연결하고 현재 브랜치를 올립니다. `YOUR_USERNAME`과 `YOUR_REPOSITORY`는 실제 값으로 바꾸세요.

   ```bash
   git remote add origin https://github.com/YOUR_USERNAME/YOUR_REPOSITORY.git
   git push -u origin main
   ```

   이미 `origin`이 있다면 추가하기 전에 `git remote -v`로 기존 연결을 확인하세요. 업로드 중 GitHub 로그인이 필요할 수 있습니다.

## 조립스페이스 자동 배포

GitHub에 코드를 올리는 것과 조립스페이스 자동 배포 연결은 별도입니다. 자동 배포를 원하면 [프로젝트 배포 설정](https://joripspace.com/projects/newstart/?tab=deployment)에서 GitHub App과 저장소, 배포 조건을 연결합니다.

`.env.joripspace`를 비롯한 환경 파일은 저장소에 올리지 않고, 서비스 키와 관리자 비밀번호는 조립스페이스의 비밀 설정에서 관리합니다.
