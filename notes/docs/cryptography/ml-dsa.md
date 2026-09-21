# ML-DSA (Module-Lattice-Based Digital Signature Algorithm)

<p class="definition">
격자(lattice) 문제의 어려움에 기반한 양자내성 전자서명 알고리즘. NIST가 <strong>FIPS 204</strong>로 표준화하였다.
</p>

## 개요

ML-DSA는 CRYSTALS-Dilithium을 기반으로 한 전자서명 표준으로, 양자 컴퓨터에 대해서도 안전할 것으로 기대되는 후양자암호(PQC) 알고리즘이다. [무결성](../information-security/cia-triad.md) 보장과 인증에 사용된다.

## 구성 (개념적 흐름)

전자서명 알고리즘은 일반적으로 세 함수로 구성된다.

```python
# 개념 설명용 의사코드 (실제 구현이 아님 — 직접 작성한 예시입니다)
def keygen():
    # 공개키/개인키 쌍 생성
    return public_key, secret_key

def sign(secret_key, message):
    # 메시지에 대한 서명 생성
    return signature

def verify(public_key, message, signature):
    # 서명 검증 (True/False)
    return is_valid
```

## 수학적 배경 (요약)

ML-DSA의 안전성은 다음 문제들의 어려움에 기반한다.

$$
\text{MLWE},\quad \text{MSIS}
$$

이들은 다항식 환 $R_q = \mathbb{Z}_q[x]/(x^n + 1)$ 위에서 정의되며, 계수 연산은 [유한체](../mathematics/finite-field.md) 개념과 밀접하다.

!!! note "표준 문서"
    공식 표준은 NIST FIPS 204에 정의되어 있다.

## 참고자료

- NIST FIPS 204 (공식 표준): [https://doi.org/10.6028/NIST.FIPS.204](https://doi.org/10.6028/NIST.FIPS.204)
- 로컬 PDF로 보관하고 싶다면 [참고자료 페이지](../refs/index.md)의 PDF 링크·임베드 방법 참고.

<div class="entry-meta">
분류: 암호 · 관련어: 전자서명, 후양자암호(PQC), 격자, FIPS 204<br>
관련 항목: <a href="../../mathematics/finite-field/">유한체</a>
</div>
