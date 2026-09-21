# 참고자료 (References)

참고 문헌과 PDF를 정리하고, 노트에서 링크·임베드하는 방법을 안내합니다.

## PDF를 다루는 세 가지 방법

### 1. 외부 링크 (DOI / URL)

가장 간단합니다. 원문이 웹에 있으면 그대로 링크합니다.

```markdown
[NIST FIPS 204](https://doi.org/10.6028/NIST.FIPS.204)
```

→ [NIST FIPS 204](https://doi.org/10.6028/NIST.FIPS.204)

### 2. 저장소에 PDF를 넣고 링크

`docs/refs/` 폴더에 PDF 파일을 넣은 뒤, 상대 경로로 링크합니다.

```markdown
[로컬 PDF 열기](example-paper.pdf)
```

파일을 `docs/refs/example-paper.pdf`로 넣으면 위 링크가 작동합니다.

### 3. 페이지 안에 PDF를 임베드(내장)

문서 안에서 바로 PDF를 보이게 하려면 아래처럼 작성합니다. (`extra.css`에 정의된 `pdf-embed` 스타일 사용)

```html
<iframe class="pdf-embed" src="example-paper.pdf"></iframe>
```

!!! warning "임베드 주의"
    임베드는 파일이 큰 경우 로딩이 느릴 수 있고, 브라우저에 따라 표시가 다를 수 있습니다. 가벼운 참조는 링크(방법 1·2)를, 핵심 자료만 임베드(방법 3)를 권장합니다.

---

## 새 항목 템플릿

새 용어를 추가할 때, 아래 내용을 복사해 해당 구역 폴더에 `파일이름.md`로 저장하세요. 그런 다음 `mkdocs.yml`의 `nav`에 한 줄 추가하면 사이드바에 나타납니다.

````markdown
# 용어명 (English Term)

<p class="definition">
여기에 한 줄 정의를 적습니다.
</p>

## 개요

상세 설명을 적습니다.

## 수식 / 증명 (필요 시)

$$
E = mc^2
$$

??? note "증명 (펼치기)"
    증명 내용을 적습니다. $\blacksquare$

## 코드 / 알고리즘 (필요 시)

```python
def example():
    return "hello"
```

## 참고자료

- [외부 링크](https://example.com)

<div class="entry-meta">
분류: (정보보안/암호/수학) · 관련어: ...<br>
관련 항목: <a href="#">다른 항목</a>
</div>
````

!!! tip "파일 이름 규칙"
    URL에 그대로 쓰이므로 **영문 소문자 + 하이픈**을 권장합니다. 예: `finite-field.md` → `.../mathematics/finite-field/`
