# CH01. Probability Theory

Created: 2022년 4월 10일 오후 10:11
Last Edited Time: 2022년 4월 11일 오전 1:05
Type: IT

# Contents

- 1.1 Probabilities
- 1.2 Events
- 1.3 Combinations of Events
- 1.4 Conditional Probability
- 1.5 Probabilities of Event Intersections
- 1.6 Posterior Probabilities

---

## 1.1.1 Introduction

- Probability theory provides the basis for the science of statistical inference through experimentation and data analysis

## 1.1.2 Sample Spaces

- **Sample Space** “집합”(전체에 대한 개념)
    - esg) The Sample spaces $S$ of an experiment is a set consisting of all the possible experimental outcomes
    - kor) 실험의 표본 공간 S는 가능한 모든 실험 결과로 구성된 집합입니다.

## 1.1.3 Probability Values

- **Probabilities**

---

A set of probability values ofr an experiment with a sample space 

$S = \left\{\ O_1, O_2, ... , O_n  \right\}$  consist of some probabilities

$P_1, P_2, ... , P_n$

that satisfy

$0 ≤ p_1 ≤ 1, 0 ≤ p_2 ≤ , ... , 0 ≤ p_n ≤ 1$

and

$p_1 + p_2 + ... + p_n = 1$

The probability of Outcome $O_i$ occuring is said to be $p_i$, and this is written

$P(O_i) = p_i$ ($O_i$가 발생할 확률)

Ex) $O_1 = 1\ P_1 = 1/6$ (1 ~ 6중에 1이 나올 확률)

---

## 1.2.1 Events and Complements

- **Events → P(A)**

> An event A is a subset of the sample space S. it collects outcomes of particular interest. The probability of an event A, P(A), is obtained by summing the probabilities of the outcomes contained within the event A.
> 

An events is said to occur if one of the outcomes contained within the event occurs

→ P(A)는 확률값들을 더한 값.

- **Complements of Events (여집합) → P(A’)**

> The event A’, the **complement** of an event A, is the event consisting  of everything in the sample space S that is not contained within the event A. In all cases
> 
> 
> $P(A) + P(A’) = 1$
> 

Events that consist of an individual outcomes are sometimes referred to as **elementary events** or **simple events**

## 1.3.1 Intersections of Events

- Intersections of Events
    
    > The Event $A \bigcap B$ is the **intersection** of the events A and B consists of the outcomes that are contained within both events A and B. The probability of this event, $P(A\cap B)$, is the probability that both events A and B occur simultaneously.
    > 
    
    $P(A \cap B) + P(A \cap B') = P(A)$$P(A \cap B) + P(A \bigcap B') = P(A)$
    

- Mutually Exclusive Events ( 공통점이 없는 경우 )
    
    > Two events A and B are said to be mutually exclusive if $A \cap B = \emptyset$ so that they have no outcomes in common.
    > 

⇒ 공통된 event가 없다.

- Some other simple results concerning the intersections
    
    > $A \cap B = B \cap A\\ A\cap S = A\\ A \cap A' = \emptyset$
    > 
    
    > $A \cap A = A\\ A\cap \emptyset = \emptyset\\ A \cap (B \cap C) = (A \cap B) \cap C)$
    > 

## 1.3.2 Unions of Events

- Unions of Events (합집합)

> The event $A \cup B$ is the union of events A and B and consists of the outcomes that are contained within at least one of the events A and B. The probability of this events, $P(A\cup B),$ is the probability that at least one of the events A and B occurs.
> 

$방법1)\ P(A\cup B) = P(A\cap B') + P(A'\cap B) + P(A\cap B$)

- Some simple results concerning the unions
    
    $방법2)\ P(A\cup B) = P(A) + P(B) - P(A\cap B)$
    
    <aside>
    💡 If the events A and B are **mutually exclusive** so that $P(A\cap B) = 0,$  then $\\ P(A\cup B) = P(A) + P(B)$
    
    </aside>
    
    $\ cf) (A\cup B)' = A'\cap B'$
    

## 1.3.3 Examples of Intersections and Unions