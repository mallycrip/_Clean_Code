> ⚰ 이 레포지토리는 수 개월간 방치가 되어 있습니다. 
## ✋ 들어가기 앞서
 본 글은 로버트 C. 마틴 저의 `Clean Code`라는 책을 바탕으로 작성하고 있습니다.<br/>
책을 읽고 이해한 내용을 바탕으로 작성하고 있어 책과 다른부분이 존재하거나 잘못된 이해한 부분이 있을 수도 있습니다. <br/>
또한 예제 코드를 `Python`으로 옮기면서 그릇되게 작성 된 부분이 있을 수 있습니다.<br/>
잘못된 부분 및 오탈자 등 수정할 부분에 대해서 `PR`, `ISSUE`를 올려주세요! 🙏<br/>
### 이 레포의 목적
   `_Clean_Code` 목적은 책 `Clean Code`를 읽을 시간이 없거나 책을 읽던 도중 이해가 되지 않는 부분에 대해서 찾아 볼 수 있도록 함에 있습니다.<br/>
 본 레포를 봄으로서 `Clean Code`를 완독하였다고 생각하시면 안됩니다. `Clean Code`에서 생략한 내용도 매우 많으며, 주관적으로 작성한 부분이 있기 때문에 일부 오개념을 습득할 수도 있습니다. 본 레포는 단순하게 참고만 하셨으면 좋겠습니다.

# CleanCode
__다음은 클린 코드를 짜기 위한 방법들이다.__
- [의미 있게 이름 정하기](https://github.com/mallycrip/_Clean_Code/tree/master/%EC%9D%98%EB%AF%B8%20%EC%9E%88%EA%B2%8C%20%EC%9D%B4%EB%A6%84%20%EC%A0%95%ED%95%98%EA%B8%B0)
- [함수 관련](https://github.com/mallycrip/_Clean_Code/tree/master/%ED%95%A8%EC%88%98)
- [주석](https://github.com/mallycrip/_Clean_Code/blob/master/%EC%A3%BC%EC%84%9D)
- [형식 맞추기](https://github.com/mallycrip/_Clean_Code/tree/master/%ED%98%95%EC%8B%9D)
- [단위 테스트](https://github.com/mallycrip/_Clean_Code/tree/master/%EB%8B%A8%EC%9C%84%20%ED%85%8C%EC%8A%A4%ED%8A%B8)
- [객체와 자료구조](https://github.com/mallycrip/_Clean_Code/tree/master/%EA%B0%9D%EC%B2%B4%EC%99%80%20%EC%9E%90%EB%A3%8C%20%EA%B5%AC%EC%A1%B0)
- [오류 처리](https://github.com/mallycrip/_Clean_Code/tree/master/%EC%98%A4%EB%A5%98%20%EC%B2%98%EB%A6%AC)
- [경계](https://github.com/mallycrip/_Clean_Code/tree/master/%EA%B2%BD%EA%B3%84)
- [클래스](https://github.com/mallycrip/_Clean_Code/tree/master/%ED%81%B4%EB%9E%98%EC%8A%A4)
## 소프트웨어는 80% 이상이 소위 유지보수이다.

### 유지보수에 초점을 맞춘 TPM의 5S원칙
- Sort (Seiri) : 적절한 명명법을 통하여 __무엇이 어디에 있는지 알아야함.__
- Set in order (Seiton) : 코드는 누구나 예상하는 위치에 있어야 함.
- Shine (Seiso) : 주석 등 쓸모 없는 부분은 제거해야 함.
- Standardize (Seiketsu) : 작업 공간을 청소하는 방식에 그룹이 동의 해야 함. 표준을 정해야 함.
- Sustain/self-discipline (Shutsuke) : 관례를 따르고 자기 작품을 자주 돌아보고, 기꺼이 변경해야 함.

### 나쁜 코드로 치르는 대가
__나쁜 코드는 개발 속도를 크게 떨어뜨린다.__
 나쁜코드는 쌓이면 쌓일수록 팀 생산성은 떨어지게 된다.<br/>
생산성이 떨어지면 관리층에서는 이를 복구하려 들것이고, 새 인력을 충원할 것이다.<br/>
하지만 새 인력은 시스템 설계에 대한 지식이 많지 않고, 생산성을 높여야 한다는 압력에 시달려 더 나쁜코드를 양산한다<br/>
<br/>
__나쁜코드를 만드는 양산하는 것은 관리자의 문제가 아니다__<br/>
 나쁜 코드의 위험을 이해하지 못하는 관리자 말을 그대로 따르는 행동이 문제이다<br/>
<br/>
__개발 속도를 빠르게, 기한을 맞추는 유일한 방법은 언제나 코드를 깨끗하게 유지하는 습관이다__<br/>
 주변코드를 읽지 않으면 새 코드를 짜지 못한다. 주변 코드가 읽기 쉬우면 새 코드 또한 짜기 쉽다. <br/>
급하다면, 쉽게짜려면, 서둘러 끝내려면 읽기 쉽게 만들면 된다.

## 프로그래머들의 정의한 깨끗한코드
- `의존성`을 최대한 줄이고 명확하게 표현한 코드
- 성능을 최적으로 유지한 코드 (속도 뿐만이 아닌 자원활용 등)
- 세세한 상황까지 주의 깊게 꼼꼼히 짠 코드
- 명쾌한 `추상화`와 단순한 제어문으로 필요한 내용만 담은 코드
- 다른 사람이 고치기 쉬운 코드
- `테스트 케이스`가 존재하고 모든 `테스트`를 통과한 코드
- 중복이 없고 클래스, 메서드, 함수 등을 최대한 줄인 코드
