## 📄 Pytorch 

<img src="https://user-images.githubusercontent.com/114068529/199400931-b39a6dea-4717-4d84-a68e-d58bd023614b.png" width=300>

> **Pytorch의 개요**

- 딥러닝을 구현하기 위한 파이썬과 토치 기반의 오픈소스 머신러닝 라이브러리
  
- 파이썬 기반의 과학 연산 패키지

  - numpy를 대체하면서 GPU를 이용한 연산이 필요한 경우 사용

  - 최대한의 유연성과 속도를 제공하는 딥러닝 연구 플랫폼이 필요한 경우 사용

  - GPU와 CPU를 사용하는 애플리케이션에 주로 사용
<br>

> **Pytorch 특징**

- 강력한 GPU 가속 지원을 갖춘 텐서 계산 

- DNN 네트워크 생성과 학습을 위한 자동 차별화

- Define by Run의 딥러닝 구현 방식 

  - Define by Run(= 동적 계산 그래프) : 딥러닝에서 수행하는 연산과 값 초기화가 동시에 실행되는 것

  - 실시간 결과값 시각화 가능

- numpy, Scipy, Cython 등 여러 라이브러리와의 높은 호환성 

- 연산속도가 빠름
<br>

> **깃허브 머신러닝 repo 갯수(2020년 6월 기준)**

![image](https://user-images.githubusercontent.com/114068529/200106470-b9add456-71a0-4e3f-b3ab-694cd987ca2a.png)
<br>

> **Pytorch 모듈**

- **torch.autograd** : 신경망 학습을 지원하는 Pytorch의 자동 미분 엔진

- **torch.optim** : 다양한 최적화 알고리즘을 구현

  - **torch.optim.SGD( )** : 한 번에 들어오는 데이터의 수대로 경사하강법 알고리즘을 적용하는 최적화 함수

  >
      torch.optim.SGD(params,lr,momentum,dampening = 0,weight_decay = 0, nesterov = False
      
  
  - **optimizer.zero_grad( )** : 반복 시에 전에 계산했던 기울기(=가중치)를 0으로 초기화하는 함수 
   
  >  
  
      optimizer = optim.SGD(model.parameters(), lr=0.1, momentum=0.9)
      optimizer.zero_grad() 
  

- **torch.nn** : Neural Network의 모든 것을 포괄하는 모든 신경망 모델의 Base Class
  
  - **nn.Sequential( )** : ReLU 같은 활성화 함수를 정렬하고 입력값이 들어오면 차례대로 함수를 실행해 결과값 반환
   
  >  
  
      import torch.nn as nn

      model = nn.Sequential(nn.Linear(6,10), nn.ReLU(10,5))
  
 
> **출처**

- [simplilearn](https://www.simplilearn.com/what-is-pytorch-article#what_is_pytorch_and_how_does_it_work)
- [Pytorch](https://pytorch.org)
