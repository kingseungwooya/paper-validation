## 논문 검증 프로그램

---

### 요구 사항 명세

- 논문에 대한 임의의 random 데이터 ( 논문 명, 저자 명,  저자 정보, I저널 정보 등 )에 대해 유효한 데이터인지 검증하는 기능 개발

---

### 기능 명세서

<aside>
💡 핵심 기능만 명세

</aside>

- 논문을 검색하는 기능
- 논문의 저자를 확인하는 기능
    - 저자의 정보를 확인하는 기능 ( 제 1 저자 or 2 저자 )
- 논문의 학회지를 검색하는 기능
    - 입력된 학회지 정보와 비교하여 확인하는 기능
    - KCI impact factor, WOS impact factor 를 확인하는 기능

---

## TestCase

1. 참 값 ( 모든 입력된 데이터가 True 값 )
    1. KCI, SCI 동시 기재되어 있는 논문 
    2. KCI 에만 기재되어 있는 논문
    3. SCI 에만 기재되어 있는 논문
    4. 둘 다 기재되어 있지 않은 논문
2. Exception
    1. 논문이 없는 경우
    2. 저자 정보가 잘못된 경우
    3. KCI 등재정보가 잘못된 경우
    4. 해외 학술지 정보가 잘못된 경우
    5. 영향력 지수가 잘못된 경우

---

### 곤란한 상황들..

- ~~Clarivate API 승인이 나지 않는다..~~
    
    → KIS API를 이용한 해결 
    
- ~~Clarivate API Free version 에는 유의미한 API 들이 없다..~~
    
    → KIS API를 이용한 해결 
    
- API를 이용한 학회지의 정보를 검색할 시에 현재 기준으로 논문의 등급을 불러옴.
    
    → 2020년에 A학회가 SCI 에 포함되었지만 2023년에 탈락할 경우에 대한 해결 부족. 
    

---

### 회고

- 곤란한 상황들에 대해 진작에 많은 예외 상황을 생각하고 TestCase를 만들고 그에 맞춰 작업했으면 뒤늦게 이런 일이 안 벌어지지 않았을까 생각한다.
- 학회의 구성 원리(?)에 대해 좀 더 알아봤으면 좋았을 것 같다.
    - 한번 SCI가 선정되면 계속 유지된다고 착각했다.
