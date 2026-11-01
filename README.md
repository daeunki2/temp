
# 개인 이력서 & 포트폴리오

MkDocs와 GitHub Pages를 활용한 개인 이력서 및 포트폴리오 웹사이트입니다.

Markdown 파일을 수정하면 웹사이트 내용을 쉽게 변경할 수 있습니다.

`main` 브랜치에 Push하면 GitHub Actions를 통해 웹사이트가 자동으로 배포됩니다.

## 1. 프로젝트 구조

```text
friend-cv/
├── .github/
│   └── workflows/
│       └── deploy.yml
├── docs/
│   ├── index.md
│   ├── about.md
│   ├── education.md
│   ├── experience.md
│   ├── projects.md
│   ├── skills.md
│   ├── contact.md
│   └── assets/
│       └── CV.pdf
├── mkdocs.yml
├── requirements.txt
└── README.md
```

### 파일 설명

| 파일 | 설명 |
|------|------|
| index.md | 메인 페이지 |
| about.md | 자기소개 |
| education.md | 학력 |
| experience.md | 경력 |
| projects.md | 프로젝트 |
| skills.md | 기술 및 역량 |
| contact.md | 연락처 |
| CV.pdf | 다운로드용 PDF 이력서 |
| mkdocs.yml | 웹사이트 설정 |
| deploy.yml | 자동 배포 설정 |

## 2. 프로젝트 내려받기

### 처음 다운로드할 때

터미널을 열고 아래 명령어를 실행합니다.

```bash
git clone https://github.com/USERNAME/friend-cv.git
cd friend-cv
```

`USERNAME`은 자신의 GitHub 사용자명으로 변경합니다.

### 이미 다운로드한 프로젝트를 최신 상태로 업데이트할 때

```bash
git pull origin main
```

GitHub에 올라온 최신 변경 사항을 내 컴퓨터로 가져옵니다.

## 3. 개발 환경 설정

Python이 설치되어 있어야 합니다.

### 가상환경 생성

```bash
python3 -m venv .venv
```

### 가상환경 실행

Mac / Linux:

```bash
source .venv/bin/activate
```

Windows:

```powershell
.venv\Scripts\Activate.ps1
```

### 필요한 패키지 설치

```bash
pip install -r requirements.txt
```

## 4. 웹사이트 실행하기

```bash
mkdocs serve
```

브라우저에서 다음 주소로 접속합니다.

http://127.0.0.1:8000

Markdown 파일을 수정하면 로컬 웹사이트에 변경 사항이 자동으로 반영됩니다.

서버를 종료하려면 `Ctrl + C`를 누릅니다.

## 5. 이력서 수정하기

`docs/` 폴더에 있는 Markdown 파일을 수정하면 됩니다.

예를 들어 자기소개를 수정하려면:

```bash
code docs/about.md
```

Markdown 작성 예시:

```markdown
# 자기소개

안녕하세요. 홍길동입니다.

## 학력

- 2020 ~ 2024: OO대학교 컴퓨터공학과

## 경력

- 2024 ~ 현재: OO회사 개발자

## 기술

- Python
- JavaScript
- SQL
```

파일을 저장하면 됩니다.

## 6. GitHub 사용법

### STEP 1. 최신 내용 내려받기 (Pull)

작업을 시작하기 전에 실행합니다.

```bash
git pull origin main
```

다른 컴퓨터에서 수정했거나 GitHub에서 직접 수정한 내용을 가져옵니다.

### STEP 2. 수정한 파일 추가하기 (Add)

파일을 수정한 후 실행합니다.

```bash
git add .
```

`.`은 현재 폴더의 모든 변경 사항을 Git에 추가한다는 의미입니다.

변경 사항을 확인하려면:

```bash
git status
```

### STEP 3. 변경 사항 저장하기 (Commit)

```bash
git commit -m "이력서 업데이트"
```

Commit은 현재 변경 사항을 하나의 기록으로 저장하는 작업입니다.

따옴표 안의 메시지는 자유롭게 작성할 수 있습니다.

예시:

```bash
git commit -m "학력 추가"
git commit -m "프로젝트 수정"
git commit -m "PDF 이력서 업데이트"
```

### STEP 4. GitHub에 업로드하기 (Push)

```bash
git push origin main
```

내 컴퓨터에서 저장한 Commit을 GitHub에 업로드합니다.

업로드가 완료되면 GitHub Actions가 자동으로 웹사이트를 빌드하고 배포합니다.

### 가장 자주 사용하는 명령어

```bash
# 1. 최신 내용 내려받기
git pull origin main

# 2. 파일 수정 후 변경 사항 추가
git add .

# 3. 변경 사항 저장
git commit -m "이력서 수정"

# 4. GitHub 업로드 및 자동 배포
git push origin main
```

## 7. PDF 이력서 다운로드 기능

PDF 이력서를 다음 위치에 저장합니다.

```text
docs/assets/CV.pdf
```

메인 페이지인 `docs/index.md`에 다음 내용을 추가합니다.

```markdown
[PDF 이력서 다운로드](assets/CV.pdf)
```

방문자가 해당 링크를 클릭하면 PDF 파일을 열거나 다운로드할 수 있습니다.

PDF 파일을 수정했다면 같은 이름으로 교체한 후 GitHub에 Push하면 됩니다.

## 8. GitHub Pages 자동 배포

이 프로젝트는 GitHub Actions를 사용하여 자동으로 배포됩니다.

### 자동 배포 과정

```text
Markdown 파일 수정
        ↓
git add .
        ↓
git commit
        ↓
git push origin main
        ↓
GitHub Actions 실행
        ↓
MkDocs 웹사이트 빌드
        ↓
GitHub Pages 자동 배포
        ↓
웹사이트 업데이트 완료
```

### 최초 1회 설정

GitHub 저장소에 접속합니다.

1. `Settings` 메뉴를 클릭합니다.
2. 왼쪽 메뉴에서 `Pages`를 선택합니다.
3. `Build and deployment` 항목을 찾습니다.
4. `Source`를 `GitHub Actions`로 변경합니다.

자동 배포 설정 파일은 다음 위치에 있어야 합니다.

```text
.github/workflows/deploy.yml
```

### 배포 확인 방법

1. GitHub 저장소에 접속합니다.
2. `Actions` 탭을 클릭합니다.
3. `Deploy MkDocs to GitHub Pages` 작업을 선택합니다.
4. 배포 성공 여부를 확인합니다.

배포가 성공하면 다음 주소에서 사이트를 확인할 수 있습니다.

https://USERNAME.github.io/friend-cv/

`USERNAME`과 `friend-cv`는 실제 GitHub 사용자명 및 저장소 이름으로 변경해야 합니다.

## 9. 자주 발생하는 문제

### git push가 실패하는 경우

먼저 최신 내용을 가져옵니다.

```bash
git pull origin main
```

충돌이 발생하면 충돌을 해결한 뒤 다시 Commit 및 Push해야 합니다.

### 변경한 내용이 웹사이트에 보이지 않는 경우

GitHub의 `Actions` 탭에서 배포가 성공했는지 확인합니다.

배포가 성공했다면 브라우저를 새로고침합니다.

### PDF가 열리지 않는 경우

다음 사항을 확인합니다.

- `docs/assets/CV.pdf` 파일이 존재하는지
- 파일 이름의 대소문자가 일치하는지
- PDF 파일이 GitHub에 Push되었는지

### 로컬 서버가 실행되지 않는 경우

가상환경이 활성화되어 있는지 확인하고 패키지를 다시 설치합니다.

```bash
pip install -r requirements.txt
mkdocs serve
```

## 10. 작업 요약

처음에는 프로젝트를 Clone하고 개발 환경을 설정합니다.

이후에는 다음 네 가지 명령어만 기억하면 됩니다.

```bash
git pull origin main
git add .
git commit -m "Update CV"
git push origin main
```

`main` 브랜치에 Push하면 웹사이트는 자동으로 배포됩니다.
