# Notes on Information Security, Cryptography, and Mathematics

MkDocs Material 기반 학술 노트 사이트입니다. 정보보안 · 암호 · 수학 세 구역으로 나누어 용어 사전, 수학 증명, 알고리즘, 참고자료를 정리합니다.

## 사전 준비

- GitHub 계정
- (로컬 미리보기용) Python 3.x

## 최초 설정 (한 번만)

1. **자리표시자 변경**: `mkdocs.yml`에서 `YOUR_USERNAME`을 본인 GitHub 사용자명으로 모두 바꿉니다. (`site_url`, `repo_url`, `repo_name`)
2. **GitHub에 저장소 생성**: 이름을 `notes`로 만듭니다. (다른 이름을 쓰면 `mkdocs.yml`의 URL과 아래 최종 주소도 그 이름에 맞춰 바뀝니다.)
3. **이 폴더 전체를 저장소에 업로드**합니다.
   - 브라우저: 저장소 → "Add file" → "Upload files"로 드래그 업로드
   - 또는 Git: `git init && git add . && git commit -m "init" && git branch -M main && git remote add origin https://github.com/YOUR_USERNAME/notes.git && git push -u origin main`
4. **GitHub Pages 소스 설정**: 저장소 → Settings → Pages → "Build and deployment" → Source를 **GitHub Actions**로 설정합니다.
5. main 브랜치에 push되면 자동으로 빌드·배포됩니다.

최종 주소: `https://YOUR_USERNAME.github.io/notes/`

## 로컬에서 미리보기

```bash
pip install -r requirements.txt
mkdocs serve
```

브라우저에서 `http://127.0.0.1:8000` 접속. 파일을 저장하면 자동 새로고침됩니다.

## 새 항목 추가하는 법

1. 해당 구역 폴더(`docs/information-security/`, `docs/cryptography/`, `docs/mathematics/`)에 `파일이름.md`를 만듭니다. (영문 소문자 + 하이픈 권장)
2. 내용은 `docs/refs/index.md` 하단의 **항목 템플릿**을 복사해 채웁니다.
3. `mkdocs.yml`의 `nav`에 해당 파일을 한 줄 추가합니다.
4. 저장 후 push하면 사이트에 반영됩니다.

## 사용법 요약

- **검색**: 상단 검색창에서 한글·영어 모두 검색됩니다.
- **새 항목 추가**: 해당 구역 폴더에 `.md` 파일을 만들고, `mkdocs.yml`의 `nav`에 한 줄 추가합니다.
- **내부 링크**: `[유한체](../mathematics/finite-field.md)` 처럼 파일 경로로 다른 항목을 연결합니다.
- **수식**: 인라인은 `$...$`, 블록은 `$$...$$` 로 작성합니다. (예: $E=mc^2$)
- **코드/알고리즘**: 삼중 백틱 코드 블록에 언어를 지정하면 문법이 강조됩니다.
- **참고 PDF**: `docs/refs/` 폴더에 PDF를 넣고 링크하거나, 외부 DOI/URL로 링크합니다.

!!! tip "항목 작성 템플릿"
    새 항목을 만들 때는 [참고자료 페이지](refs/index.md) 하단의 **항목 템플릿**을 복사해서 시작하세요.

## 주요 기능

- 한글·영어 검색
- 라이트/다크 모드
- 수식(LaTeX): 인라인 `$...$`, 블록 `$$...$$`
- 코드 블록 문법 강조 + 복사 버튼
- 접이식 증명 상자, 참고/경고 콜아웃
- 각 문서 편집 링크(GitHub로 바로 이동)
- 참고 PDF 링크 및 임베드 (`docs/refs/index.md` 참고)

## 폴더 구조

```
notes/
├─ mkdocs.yml                  # 사이트 설정
├─ requirements.txt
├─ README.md
├─ .gitignore
├─ .github/workflows/deploy.yml   # 자동 배포
└─ docs/
   ├─ index.md                 # 홈
   ├─ javascripts/mathjax.js   # 수식 렌더링
   ├─ stylesheets/extra.css    # 사용자 정의 스타일
   ├─ information-security/
   ├─ cryptography/
   ├─ mathematics/
   └─ refs/                    # 참고자료 + PDF 저장 위치
```
