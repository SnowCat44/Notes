# 대수학 (Algebra)

<p class="definition">
원소의 개수가 유한한 <a href="#">체(field)</a>. 갈루아 체(Galois Field)라고도 하며 $\mathrm{GF}(q)$ 또는 $\mathbb{F}_q$로 표기한다.
</p>

## 정의

체 $F$가 유한개의 원소를 가지면 이를 **유한체**라 한다. 유한체의 원소 개수는 항상 소수 $p$의 거듭제곱 $q = p^n$ 형태이며, 각 $q$에 대해 동형(isomorphism)을 무시하면 유한체는 유일하게 존재한다.

## 성질

- 덧셈과 곱셈에 대해 닫혀 있고, $0$이 아닌 원소들은 곱셈에 대한 [군](#)을 이룬다.
- 표수(characteristic)는 소수 $p$이다.
- 곱셈군 $\mathbb{F}_q^{\times}$는 위수 $q-1$인 순환군이다.

## 정리와 증명 예시

!!! abstract "정리"
    유한체 $\mathbb{F}_q$의 곱셈군 $\mathbb{F}_q^{\times}$는 순환군이다.

??? note "증명 (펼치기)"
    $\mathbb{F}_q^{\times}$는 위수 $q-1$인 유한 아벨군이다. 임의의 $d \mid (q-1)$에 대해, 방정식

    $$
    x^d = 1
    $$

    은 체 $\mathbb{F}_q$에서 많아야 $d$개의 해를 가진다(차수 $d$인 다항식의 근은 최대 $d$개). 유한 아벨군에서 각 위수 $d$의 원소 개수에 대한 이 조건은 그 군이 순환군임을 함의한다. 따라서 $\mathbb{F}_q^{\times}$는 순환군이다. $\blacksquare$

## 암호에서의 활용

유한체 위의 연산은 [ML-DSA](../cryptography/ml-dsa.md)를 비롯한 여러 암호 알고리즘의 기반이 된다.

<div class="entry-meta">
분류: 수학 · 관련어: 체, 군, 갈루아 체, 순환군<br>
관련 항목: <a href="../../cryptography/ml-dsa/">ML-DSA</a>
</div>
