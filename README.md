## 논문 검증 프로그램

---

### 요구 사항 명세

- 논문에 대한 임의의 random 데이터 ( 논문명, 저자명, 학술지, IF, 인용횟수 등 )에 대해 유효한 데이터인지 검증하는 기능 제작

---

### 기능 명세서

<aside>
💡 핵심 기능만 우선 명세

</aside>

- KCI API를 이용해 논문 정보 validation 기능
- Clarivate API를 이용해 journal에 대한 정보 validation 기능

---

### 진행 완료된 작업

- [ ]  KCI API key 발급
- [ ]  KCI API 를 이용해 논문 정보 탐색 api testing
- [ ]  Clarivate API key 신청,.. → 대기중

### 추후 예정 계획

- Clarivate api testing
- 임의의 데이터를 이용하여 전체적인 workflow 구현해보기
- 예외처리, 버그찾기
- 문서화
