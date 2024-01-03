# AIFFEL Campus Online Code Peer Review Templete
- 코더 : 전휘호
- 리뷰어 : 이승제


# PRT(Peer Review Template)
- [x]  **1. 주어진 문제를 해결하는 완성된 코드가 제출되었나요?**
    - 문제에서 요구하는 최종 결과물이 첨부되었는지 확인
    - 문제를 해결하는 완성된 코드란 프로젝트 루브릭 3개 중 2개, 퀘스트 문제 요구조건 등을 지칭  
        - CAM을 얻기 위한 기본모델의 구성과 학습이 정상 진행되었는가?
     
![image](https://github.com/huihojeun2/EXPLORATION/assets/85716670/f07bb72a-ce5a-4671-aa37-72bb813a6b4b)

        - 분류근거를 설명 가능한 Class activation map을 얻을 수 있는가?

![image](https://github.com/huihojeun2/EXPLORATION/assets/85716670/2c7723c6-7344-4d97-a49a-2b819d0b4689)
        
        - 인식결과의 시각화 및 성능 분석을 적절히 수행하였는가?
     
![image](https://github.com/huihojeun2/EXPLORATION/assets/85716670/3b5a57cd-28fc-49fe-aa3c-cbb109b3c265)

![image](https://github.com/huihojeun2/EXPLORATION/assets/85716670/3758fc1d-ed2c-49bc-8f22-243aca532f0f)


-> 2개 이상의 퀘스트 요구조건을 달성하였다.
    
- [x]  **2. 전체 코드에서 가장 핵심적이거나 가장 복잡하고 이해하기 어려운 부분에 작성된 
주석 또는 doc string을 보고 해당 코드가 잘 이해되었나요?**
    - 해당 코드 블럭에 doc string/annotation이 달려 있는지 확인
    - 해당 코드가 무슨 기능을 하는지, 왜 그렇게 짜여진건지, 작동 메커니즘이 뭔지 기술.
    - 주석을 보고 코드 이해가 잘 되었는지 확인

![image](https://github.com/huihojeun2/EXPLORATION/assets/85716670/889182aa-96fe-45ec-9bfc-5dfea8e127f6)

-> 주석이 잘 달려있어서 어떤 기능을 하는지 파악하기 쉬웠다.

        
- [x]  **3. 에러가 난 부분을 디버깅하여 문제를 “해결한 기록을 남겼거나” 
”새로운 시도 또는 추가 실험을 수행”해봤나요?**
    - 문제 원인 및 해결 과정을 잘 기록하였는지 확인
    - 문제에서 요구하는 조건에 더해 추가적으로 수행한 나만의 시도, 실험이 기록되어 있는지 확인
     
![image](https://github.com/huihojeun2/EXPLORATION/assets/85716670/b75aa4d9-240d-413f-95a1-4f9e8b69d447)

-> 바운딩 박스를 찾지 못한 경우를 처리하는 것을 볼 수 있다
        
- [x]  **4. 회고를 잘 작성했나요?**
    - 주어진 문제를 해결하는 완성된 코드 내지 프로젝트 결과물에 대해
    배운점과 아쉬운점, 느낀점 등이 기록되어 있는지 확인
    - 전체 코드 실행 플로우를 그래프로 그려서 이해를 돕고 있는지 확인

![image](https://github.com/huihojeun2/EXPLORATION/assets/85716670/7aa1ffa6-5427-4c55-8570-a5d1ad056c36)

-> 회고가 잘 작성된 것을 볼 수 있다.

        
- [x]  **5. 코드가 간결하고 효율적인가요?**
    - 파이썬 스타일 가이드 (PEP8) 를 준수하였는지 확인
    - 하드코딩을 하지않고 함수화, 모듈화가 가능한 부분은 함수를 만들거나 클래스로 짰는지
    - 코드 중복을 최소화하고 범용적으로 사용할 수 있도록 함수화했는지

![image](https://github.com/huihojeun2/EXPLORATION/assets/85716670/3b0e6cb1-03b4-4fdf-ab72-84e44aa2ecad)

-> 함수화로 중복된 코드를 줄일 수 있었다.
