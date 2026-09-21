# Notes on Information Security, Cryptography, and Mathematics


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
