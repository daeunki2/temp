
## 내 이력서 웹사이트 만들기

이 저장소는 개인 이력서 웹사이트 템플릿입니다.

### 1. 템플릿 복사하기

1. [원본 저장소](https://github.com/daeunki2/temp)에 접속합니다.
2. `Use this template` 버튼을 클릭합니다.
3. `Create a new repository`를 선택합니다.
4. 자신의 GitHub 계정을 선택합니다.
5. 원하는 저장소 이름을 입력합니다.
6. `Create repository`를 클릭합니다.

이제 자신의 GitHub에 독립적인 이력서 저장소가 생성됩니다.

### 2. GitHub Pages 설정하기

본인의 저장소에서:

1. `Settings` 클릭
2. `Pages` 클릭
3. `Build and deployment`의 `Source`를 `GitHub Actions`로 설정

### 3. 내 컴퓨터로 다운로드하기

```bash
git clone https://github.com/USERNAME/REPOSITORY.git
cd REPOSITORY
```

USERNAME은 자신의 GitHub 사용자명,
REPOSITORY는 생성한 저장소 이름으로 변경합니다.

### 4. 이력서 수정하기

`docs/` 폴더 안의 Markdown 파일을 수정합니다.

- index.md: 메인 페이지
- about.md: 자기소개
- education.md: 학력
- experience.md: 경력
- projects.md: 프로젝트
- skills.md: 기술 및 역량
- contact.md: 연락처

PDF 이력서는 `docs/assets/CV.pdf`에 넣습니다.

### 5. 수정 사항 업로드하기

```bash
git pull origin main
git add .
git commit -m "이력서 수정"
git push origin main
```

### 6. 자동 배포

`main` 브랜치에 Push하면 GitHub Actions가 자동 실행됩니다.

배포 상태는 GitHub 저장소의 `Actions` 탭에서 확인할 수 있습니다.

배포된 웹사이트 주소:

https://USERNAME.github.io/REPOSITORY/

### 7. 이후 업데이트

앞으로는 Markdown 파일을 수정하고 Push만 하면 됩니다.

```bash
git add .
git commit -m "Update CV"
git push origin main
```

별도의 배포 명령어는 필요하지 않습니다.
