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

!!! info "작성 규칙"
    출처·최종 수정일 표기의 상세 규칙은 저장소의 `docs/conventions.md`를 따릅니다. 아래 템플릿은 그 규칙을 이미 반영한 것입니다.

````markdown
# 용어명 (English Term)

*최종 수정일: 2026-09-21*

<p class="definition">
여기에 한 줄 정의를 적습니다.
</p>

## 개요

상세 설명을 적습니다. 사실 주장에는 각주로 출처를 답니다.[^ref1]
시간에 따라 변하는 값(표준 버전·권고값 등)은 문장 각주에 확인일을 남깁니다.[^ref2]

## 수식 / 증명 (필요 시)

$$
E = mc^2
$$

??? note "증명 (펼치기)"
    증명 내용을 적습니다. $\blacksquare$

## 코드 / 알고리즘 (필요 시)

아래 예시는 개념 설명용으로 직접 작성한 것입니다.[^own]

```python
def example():
    return "hello"
```

## 출처 (References)

- (이 페이지의 포괄적 참고문헌을 정리합니다. 각주는 아래에 자동으로 렌더링됩니다.)

[^ref1]: 저자/기관, *문서명*, 발행일. DOI 또는 URL <https://example.com> (accessed 2026-09-21).
[^ref2]: 저자/기관, *문서명*, 발행일. 확인일 2026-09-21.
[^own]: 직접 작성 (2026-09-21). 특정 문헌을 그대로 옮긴 것이 아님.

<div class="entry-meta">
분류: (정보보안/암호/수학) · 관련어: ...<br>
관련 항목: <a href="#">다른 항목</a>
</div>
````

!!! tip "파일 이름 규칙"
    URL에 그대로 쓰이므로 **영문 소문자 + 하이픈**을 권장합니다. 예: `finite-field.md` → `.../mathematics/finite-field/`

## 출처·수정일 표기 빠른 참고

- **페이지 최종 수정일**: 제목 바로 아래 `*최종 수정일: YYYY-MM-DD*`
- **문장 출처**: 문장 끝에 `[^식별자]`, 페이지 하단에 각주 내용
- **웹·URL 출처**: 접근일 `(accessed YYYY-MM-DD)` 필수
- **직접 작성/추론**: `[^own]` 같은 각주로 출처 없음을 명시
- **날짜 형식**: 항상 `YYYY-MM-DD` (ISO 8601)
- 전체 규칙: `docs/conventions.md`
