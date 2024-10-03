# DT_Task_Offloading
Digital Twin task offloading with partial offloading and edge collaboration

일반적으로 디지털 트윈 환경에서 사용되는 IoT task offloading 방식은 partial offfloading이나 edge collaboration 방식만을 적용하여 최적화하는 경우가 많다.

하지만 B5G(Beyond 5G)나 6G환경에서 네트워크는 저지연을 요구하고 이는 지연시간을 최적화하는것이 더 중요하다는 것을 의미한다.

또한 디지털 트윈의 결과값만을 구하고 적용하지, 최적화하는데 걸리는 지연시간을 적용하는 방법을 적용한 경우도 없기 때문에 이번 논문에서는 이를 적용하려고 한다.

제안하려는 구조는 다음과 같다.

![image](https://github.com/user-attachments/assets/e6afa82f-9432-4288-abc6-e1ef37a4a034)

제안하는 구조에 따라서 각각 DT를 생성하는 데 걸리는 시간인 DT placement와 이렇게 DT에서 각 IoT network를 본 딴 가상의 객체들의 task offloading을 최소화하기 위한 최적화 시뮬레이션, 그리고 이렇게 정해진 결과값을 반영하여 task offloading하는데 걸리는 지연시간을 구하는 Physical Task Offloading.

이렇게 3가지 단계를 메타 휴리스틱 알고리즘을 적용시켜보고 Baseline 알고리즘들과 성능을 비교해보고자 한다.

Baseline 알고리즘은 3가지가 존재한다.

1. 로컬에서 처리하는 방밥

2. Edge server에서 처리하는 방법

3. 강화학습을 적용한 방법(Q-learning)

1, 2는 전부다 유명한 방법들이기 때문에, Q-learning 방식만 설명하자면 다음과 같다.

![image](https://github.com/user-attachments/assets/cff6f9c6-758a-4b9f-ba13-e83201c00a25)

이를 각각 메타 휴리스틱 알고리즘인 GA, SA, PSO 알고리즘과 성능을 비교한다.

![image](https://github.com/user-attachments/assets/369938a8-6ba0-4665-bd80-a9b2b95697d1)

![image](https://github.com/user-attachments/assets/1a4e517c-e3a1-4fa4-9580-b54afb33f872)

메타 휴리스틱 알고리즘과 Baseline 알고리즘들과 전체 지연시간을 비교하면 다음과 같다.

![image](https://github.com/user-attachments/assets/015b4528-ed49-484e-8995-c8fd182fc49c)

