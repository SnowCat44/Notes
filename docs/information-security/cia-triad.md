# CIA 3요소 (CIA Triad)

<p class="definition">
정보보안의 세 가지 핵심 목표인 <strong>기밀성(Confidentiality)</strong>, <strong>무결성(Integrity)</strong>, <strong>가용성(Availability)</strong>을 묶어 이르는 모델.
</p>

## 개요

CIA 3요소는 정보보안 정책과 통제를 설계할 때 기준이 되는 세 가지 속성이다. 어떤 보안 조치든 이 셋 중 하나 이상을 보호하기 위한 것으로 볼 수 있다.

## 세 요소

- **기밀성 (Confidentiality)**: 인가된 주체만 정보에 접근할 수 있어야 한다. 관련 기술: [암호화](../cryptography/index.md), 접근 제어.
- **무결성 (Integrity)**: 정보가 인가되지 않은 방식으로 변경되지 않아야 한다. 관련 기술: 해시, 전자서명 → [ML-DSA](../cryptography/ml-dsa.md).
- **가용성 (Availability)**: 인가된 주체가 필요할 때 정보에 접근할 수 있어야 한다.

!!! note "관련 개념"
    무결성 보장에는 수학적으로 [유한체](../mathematics/finite-field.md) 위에서 정의되는 여러 암호 알고리즘이 쓰인다.

!!! example "예시"
    - 기밀성 위반: 도청으로 평문이 노출됨
    - 무결성 위반: 전송 중 메시지가 변조됨
    - 가용성 위반: DDoS로 서비스가 중단됨

<div class="entry-meta">
분류: 정보보안 · 관련어: 기밀성, 무결성, 가용성, 접근제어<br>
참고: <a href="../../references/">References</a>
</div>
