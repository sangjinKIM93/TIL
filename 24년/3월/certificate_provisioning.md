CI/CD 환경을 재구축하는 과정에서 인증서 관련 다시 셋팅을 하는데

관련 개념과 방법들이 희미해져 다시금 정리하는 차원에서 글 작성

<br>

### 서명이란?

개발, 배포를 해도 되는 사람인지 확인

‘너는 애플로부터 인증을 받은 사람인가?’

<br>

### Automatically manage signing

- Automatically Signing 하면 기본적으로 development, distribution 인증서 모두 만들어줌
- 자동으로 해주기 때문에 크게 신경쓰지 않아도 서명과 인증이 됨

- <br>

그래도 간단하게 개념 알아보기

<br>

## Certificate

애플에서 인증한 개발자가 되보자

<br>

### CSR

- 인증 서명 요청
- 인증서를 위한 신청서

<br>

### 인증서

- 애플에서 발급
- 다운 받아서 로컬 키체인에 저장

<br>

### 서명된 인증서

다운한 인증서에 CSR 반영

CSR로 신청서를 작성하고

애플 사이트에서 인증서를 다운 받아 

신청서와 인증서를 연결함으로써 서명된 인증서를 쓸 수 있는 구조다.

이 서명된 인증서를 바탕으로 앱을 수정할 수 있는 권한을 얻게 됨

<br>

## Provisioning Profile

키체인에 있는 서명 인증서로 앱을 서명하면 믿을 수 있나?

추가적인 정보가 필요함. 앱을 실행할때의 환경(제약) 조건을 명시

- 어느 디바이스?
- 언제?
- 앱의 권한?

<br>

### Certificate vs Provisioning Profile

- “너가 믿을만한 사람인가?”
- “앱이 실행될 수 있는 환경인가?”

<br>
<br>
<br>


### 배포 자동화

‘CI/CD 구축시 어떤 인증서를 어떻게 전달해야할까?’

- Automatically Sign 로 자동으로 가능
- distribution은 Xcode > account 에서 + 버튼으로도 추가 가능
 

‘애플 계정은 뭐로 해야하지?’

- 공용 계정으로 하는게 좋지

<br>

### 참고

https://dchkang83.tistory.com/139

[https://sujinnaljin.medium.com/ios-certificate-와-provisioning-profile-e1b9455e8a51](https://sujinnaljin.medium.com/ios-certificate-%EC%99%80-provisioning-profile-e1b9455e8a51)

