
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


--------------------------------------


## 최초 1회 GitHub Pages 배포 설정

이 설정은 자신의 GitHub 저장소를 생성한 후 **최초 한 번만** 진행하면 됩니다.

### 1. GitHub Pages 활성화

1. GitHub에서 자신의 저장소에 접속합니다.
2. 상단의 `Settings`를 클릭합니다.
3. 왼쪽 메뉴에서 `Pages`를 선택합니다.
4. `Build and deployment` 항목을 찾습니다.
5. `Source`를 `GitHub Actions`로 변경합니다.

### 2. 최초 배포 실행

1. 저장소 상단의 `Actions` 탭을 클릭합니다.
2. `Deploy MkDocs to GitHub Pages`를 선택합니다.
3. `Run workflow` 버튼을 클릭합니다.
4. 브랜치를 `main`으로 선택합니다.
5. `Run workflow`를 클릭하여 배포를 시작합니다.
6. 초록색 체크 표시가 나오면 배포 성공입니다.

### 3. 웹사이트 접속

배포가 완료되면 다음 주소에서 웹사이트를 확인할 수 있습니다.

https://USERNAME.github.io/REPOSITORY/

- `USERNAME`: 자신의 GitHub 사용자명
- `REPOSITORY`: 자신의 저장소 이름

### 4. 이후 자동 배포

최초 설정 이후에는 Markdown 파일을 수정하고 `main` 브랜치에 Push하면 자동으로 배포됩니다.

```bash
git pull origin main
git add .
git commit -m "이력서 수정"
git push origin main
```

GitHub Actions가 자동으로 웹사이트를 빌드하고 배포하므로 별도의 배포 명령어는 필요하지 않습니다.

배포 상태는 GitHub 저장소의 `Actions` 탭에서 확인할 수 있습니다.
