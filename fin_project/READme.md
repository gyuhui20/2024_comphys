# Simple recharge oscillator model of ENSO using Physical-informed neural network
-> 데이터에 100%의존하지 않고, 우리가 선험적으로 알고 있는 지식을 통해서 보다 적은 수의 데이터를 활용(imbalanced data, data shortage)하면서 기존에 알고 있는 지식에도 부합하게 하는 것  

학습의 결과로 미분방정식의 predict value(graph of function)를 얻자. 단, 그 결과가 기존 loss를 계산하는 방식으로 얻는 loss를 최소화함과 동시에 방정식에 넣었을 때도 타당한 값이 나와야 한다.  
loss function =  mse(initial conition과)  + mse(pinn이 예측한 값을 t에 대해 미분한 식과 주어진 dy(방정식) 사이의 차이)  

그러려면, real value(function)을 알고 있어야함 -> 그래서 미방 풀이 진행  

Q1 . 만약 여기에 noisy measurement까지 추가한다면? 0에서1사이의 랜덤값을 추가해주자.

Q2 . 만약 loss fn의 importance of each term이 다르다면? 각각 hyperparam붙여서 기여도를 컨트롤해야함

- PINN : physical-informed neural network  
- ODE : ordinary differential equation   
- ENSO : 엘니뇨 남방 진동   
- ROM : recharge oscillator model  


