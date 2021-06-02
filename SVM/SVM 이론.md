# 1. Linear SVM : Hard Margin SVM

## 1. SVM (서포트 벡터 머신) 이란?
- 널리 사용되는 기계학습 방법론
- 패턴 인식, 자료 분석을 위한 **지도학습 모델**
- 분류와 회귀 문제에 사용 (주로는 분류 문제)
- 비-확률적 이진 선형 분류 모델
- 커널 트릭을 활용하여 비선형 분류 문제에도 사용 가능
- 학습 방향 : **마진의 최대화** (결정 경계는 주변 데이터와의 거리가 최대가 되어야 함)

![image](https://user-images.githubusercontent.com/70889699/120518516-a150a280-c40c-11eb-9a6f-d955b2d21d6d.png)

## 2. 용어
### 1) 결정 경계 (Hyperplane)
- 서로 다른 클래스를 완벽하게 분류하는 기준
- 데이터 임베딩 공간보다 1차원 낮은 부분 공간 (e.g. 2차원 데이터 공간의 결정 경계: 직선)

![image](https://user-images.githubusercontent.com/70889699/120518792-e7a60180-c40c-11eb-84d1-065a7050cf63.png)

### 2) 서포트 벡터 (Support Vector)
: 결정 경계선에 가장 가까이에 있는 각 클래스의 데이터 (여러개 있을 수 있음)

### 3) 마진 (Margin)
: 어떤 데이터도 포함하지 않는 영역, 서포트 벡터와 직교하는 직선과의 거리

![image](https://user-images.githubusercontent.com/70889699/120518928-0efcce80-c40d-11eb-9001-8f209110732f.png)

## 3. 수학적 표현
![image](https://user-images.githubusercontent.com/70889699/120518989-20de7180-c40d-11eb-9819-d956c8d0a587.png)

![image](https://user-images.githubusercontent.com/70889699/120519081-33f14180-c40d-11eb-9c6c-217d5fdea801.png)

## 4. SVM의 목적 함수 : 마진의 최대화

![image](https://user-images.githubusercontent.com/70889699/120519149-466b7b00-c40d-11eb-9877-9bea67996303.png)

## 5. Hard Margin SVM
![image](https://user-images.githubusercontent.com/70889699/120519329-7286fc00-c40d-11eb-82a0-2f0c04ae346f.png)

![image](https://user-images.githubusercontent.com/70889699/120519374-7dda2780-c40d-11eb-8cbb-b1a988d37aff.png)

![image](https://user-images.githubusercontent.com/70889699/120519405-8af71680-c40d-11eb-8878-48a93d278e39.png)


# 2. Linear SVM : Soft Margin SVM
## 1. Hard Margin SVM vs Soft Margin SVM
- Hard Margin SVM
  - 선형 분리 가능한 문제
- Soft Margin SVM
  - 선형 분리 불가능 문제
  - 에러를 허용하자!

![image](https://user-images.githubusercontent.com/70889699/120519648-d1e50c00-c40d-11eb-89a7-ee7e5f37f297.png)

## 2. Soft Margin SVM

![image](https://user-images.githubusercontent.com/70889699/120519748-f2ad6180-c40d-11eb-99bc-92cfd906bd6f.png)

![image](https://user-images.githubusercontent.com/70889699/120519765-f93bd900-c40d-11eb-97d6-ffee21b21983.png)

![image](https://user-images.githubusercontent.com/70889699/120519790-00fb7d80-c40e-11eb-9377-b0cde253f038.png)

![image](https://user-images.githubusercontent.com/70889699/120519816-0b1d7c00-c40e-11eb-8d1f-4e5792c08449.png)


# 3. Nonlinear SVM : Kernel SVM
## 1. 선형 SVM vs 비선형 SVM
- 선형 SVM : 하드 마진 SVM, 소프트 마진 SVM
- 비선형 SVM, 커널 SVM

![image](https://user-images.githubusercontent.com/70889699/120519982-3c964780-c40e-11eb-8d13-7badcbb3de07.png)

## 2. 비선형 SVM
- 데이터를 선형으로 분류하기 위해 차원을 높이는 방법 사용
- Feature Map을 통해 차원을 높임
- 커널은 Feature Map의 내적

![image](https://user-images.githubusercontent.com/70889699/120520068-5899e900-c40e-11eb-8978-4dd129cb132e.png)

## 3. 비선형 SVM의 해법
- SVM 모델을 Original Space가 아닌 Feature Space에서 학습
- Original Space에서 비선형 결정 경계 -> Feature Space에서 선형 결정 경계
- 고차원 Feature Space에서는 분류가 더 쉬울 수 있음을 입증 함

## 4. 비선형 SVM의 목적함수
![image](https://user-images.githubusercontent.com/70889699/120520316-9ac32a80-c40e-11eb-837d-3ca4c3827d38.png)

## 5. Kernel Mapping
![image](https://user-images.githubusercontent.com/70889699/120520377-aca4cd80-c40e-11eb-8a8b-1eee263e7d7b.png)

## 6. Kernel Function
![image](https://user-images.githubusercontent.com/70889699/120520420-bb8b8000-c40e-11eb-9736-dfb8b729fd7e.png)

## 7. 비선형 SVM의 예
![image](https://user-images.githubusercontent.com/70889699/120520475-cc3bf600-c40e-11eb-9821-2aa5e0fc94eb.png)

![image](https://user-images.githubusercontent.com/70889699/120520526-dbbb3f00-c40e-11eb-92d3-c8cce50b81c0.png)

![image](https://user-images.githubusercontent.com/70889699/120520551-e4137a00-c40e-11eb-930e-bf921708d2dd.png)

## 8. 비선형 SVM의 커널 선정 법
- SVM 커널을 결정하는 것은 어려운 문제! : 정해진 기준이 없으므로 실험적으로 결정
- 데이터의 특성에 맞는 커널을 결정하는 것은 중요함


# 4. SVM 다계층 분류 (Multi-Classification) 
## 1. OvR (One-vs-Rest) or OvO (One-vs-One)
- OvR (One-vs-Rest, 하나-나머지 방법) : 이항 분류 값이 가장 큰 값을 그룹으로 할당
- OvO (One-vs-One, 하나-하나 방법) : 주어진 특성 자료에 대해 가장 많이 할당된 그룹으로 할당 (voting 방식)

![image](https://user-images.githubusercontent.com/70889699/120520956-613eef00-c40f-11eb-9c9c-a1fc1ce7f0c0.png)





