# Today I Learned (TIL)

이전까지는 기술을 카테고리별로  정리하였으나 앞으로 이는 [블로그](http://jhleed.tistory.com/)에 남기기로 하고 [초보몽키님의 6개월간의 TIL 회고](https://wayhome25.github.io/til/2017/08/14/TIL-for-6-months/)를 참고하여 개발과 관련하여 학습한 내역을 일기 형식으로 적기로 하였습니다.  
## 2017년 09월

### 17.09.03 (일)

**Jenkins**
- 개인 AWS 에 CI를 설치하였습니다. [잘 정리된 메뉴얼](http://sanketdangi.com/post/62715793234/install-configure-jenkins-on-amazon-linux)을 따라하다보니 그렇게 어렵지 않게 설치 할 수 있었습니다. 개인 프로젝트에 적용할 [지속적 배포(Continuous delivery, CD)](https://aws.amazon.com/ko/devops/continuous-delivery/)의 첫 걸음이 되었으면 합니다.

**SMS (Simple Message Server)**
- 메일을 전송해주는 심플한 서버를 생성하였습니다. 어렵지 않은 작업이었지만 이전에 메일 서버를 만들어 본 적이 없었기에 의미가 있었습니다. 다음번에는 SMS를 전송해주는 서버를 만들어보려고 합니다. 

### 17.09.02 (토)

**Algorithm**
- hackerrank에서 문제를 조금 풀어보았습니다. 30 days of code라는 기본 튜토리얼인데 하루에 1개씩 문제를 제공해줍니다. 현재 2일차까지 풀었는데 문제 자체는 매우 쉽습니다. 이 코스는 아마 입문자를 대상으로 한 것 같습니다. 그러나 영어를 해석하는데에 시간이 조금 걸리긴 합니다. 개발자에게도 영어공부가 꾸준히 필요한 것을 체감합니다. 입문자 레벨을 그만 공부하고 Data structure / Algorithm 을 중급과정부터 풀어보고 싶은데 한번 시작했기 때문에 어떻게든 끝내보고 싶은 오기도 생기게 되네요.

---
### 17.09.01 (금)
- **실서버의 데이터를 대량으로 수정할 일이 생겼습니다.** 현재 사용하고 있는 MongoDB의 특성상 한번에 쿼리를 날려 변경하는 것이 불가능하였고 (스크립트를 사용한다면 되긴 하지만) 이런 요구사항이 언제 다시 발생할 지 모르기 때문에 직접 코드를 수정하는 로직을 API 서버에 작성하였습니다. 프로덕션 데이터를 수정한다는 것은 매우 민감한 일이였기에 테스트 코드를 단계별로 작성하고, 잘못되었을 경우를 대비해서 원래 상태로 돌려놓는 리커버리 코드도 작성하였습니다. 데이터베이스에 접근하기 때문에 단위 테스트를 한번 돌릴때 5분정도가 소요되었습니다. 현재 읽고 있는 `Effective Unit Testing` 에서는 단위 테스트를 작성할때에 데이터베이스 접근을 피하는 것을 권고하는데 이런 경우에는 어떻게 해결해야 할지 알아봐야겠습니다.
- 동료인 태환님으로부터 알고리즘 연습 등을 할 수 있는 사이트인 [hackerrank](https://www.hackerrank.com)를 소개받았습니다. 단순히 알고리즘등을 연습할 수 있는 것이 아니라. 특정 회사들에서 알고리즘 대회 등을 주최하는데 여기에서 우수한 성적을 올리면 상금 등으로 보상을 주거나 라이센스를 줘서 입사시 혜택을 받을 수가 있다고 합니다. 알고리즘 연습에 외재적 보상이 따르면 동기부여에 보탬이 될 것 같습니다.

## 2017년 08월

### 17.08.31 (목)

- 여전히 `MongoDB Replica Set`과 씨름을 하였습니다. AWS에 떠있는 3대의 서버 중 1대에 제대로 네트워크가 연결이 되지 않는 현상이 발견되었습니다. 공식 메뉴얼대로 똑같이 따라했는데 안되면 어디서부터 잘못됬는지 찾기 어렵고 참 난감합니다.
- `AWS`에 `부트스트래핑`이라는게 있다는 것을 팀원분에게 들었습니다. 또 멀티 인스턴스에 동시에 커맨드를 날릴 수 있는 기능도 있다고 합니다.  AWS 는 정말 편한 클라우드 서비스이면서 배울 것도 참 많은 것 같습니다.
- 조대협님께서 쓰신 [대용량 아키텍쳐와 성능 튜닝](http://www.yes24.com/24/goods/17018954) 책을 빌렸습니다. 전부 이해하기에는 아직 어렵고 REST API 설계와 NoSQL 설계 부분을 참고해보려고 합니다.

---
### 17.08.30 (수)

- 주로 `MongoDB Replica Set` 을 학습하고, 설정하는데에 많은 시간을 사용했습니다.
- 화요일에 고민했었던 프로젝트를 결국 NodeJS + Polymer Library로 구성하기로 했습니다. 프론트의 비중이 큰 프로젝트이므로 Node로 가볍게 라우팅만 해주는 기능을 제공하고 백엔드 로직은 별도의 서버에서 처리하여 API 형식으로 제공받는 것으로 결론지었습니다.

---
### 17.08.29 (화)
- 크리스티나 초도로우의 `MongoDB 완벽 가이드`라는 책을 참고하여 MongoDB Replication Set을 공부하고 있습니다. 간단한 Example을 만드는 것까지는 간단했는데 실제로 구상하려니까 고려사항이 많은 것 같습니다.
- 개발자커리어 Young Community 연합세미나 이력서 피드백을 정리하여 [블로그에 포스팅](http://jhleed.tistory.com/97)하고 페이스북에 공유했는데 생각했던 것보다 많은 분들(1000분)이 블로그를 방문해주셨습니다. 
- 회사에서 진행하고 있는 프로젝트의 Back end 로 NodeJs를 쓸지, Spring boot를 쓸지 고민이 됩니다. (Front end는 Polymer 라이브러리를 사용)
	- 가벼운 경량 백 엔드로 NodeJs 를 사용하고 싶으나 NodeJs 에 익숙하지 않음
	- 차라리 익숙한 Spring을 쓰는 것이 생산성이 나을 듯한데 그나마 그중 가볍게 사용할 수 있는 Spring Boot을 사용하려고 함
	- 고민 1 : View 단은 JSP를 사용하게 될 듯한데 Web Component Library인 Polymer와 올바른 궁합인가? (HTML import)
		- JSP가 아니라 thymeleaf를 사용하는 방법도 고려해 볼 것
	- 고민 2 : WAS는 정적 자원을 제공하는데 최적화되어있지 않다. 이 문제는 어떻게 해결해야 하는가.

---
### 17.08.28 (월)

[Polymer의 style 부분을 학습하고 정리하였습니다.](https://github.com/jhleed/study-polymer/tree/master/style)

개인적으로 사용하는 REST API 서버의 프레임워크를 spring에서 spring boot로 변경하였습니다.
별다른 충돌 없이 매끄럽게 변경되었습니다. git에서 ignoring하는 JRebel의 rebel.xml 부분만 조금 신경썼으면 완벽했을 것 같습니다.

대학을 졸업하고 첫 직장에서 개발을 처음 알려주신 [넷스루의 오재훈 개발이사님](https://www.facebook.com/jaehoon.oh.503)과 저녁을 먹었습니다.
테스트와 소프트웨어의 품질, 개발 문화에 대한 이야기를 나누었고 아주 재밌었습니다.

---
### 17.08.27 (일)

어제 개발자커리어 세미나를 다녀오고 나서 github, blog를 재정비해야 되겠다고 생각했습니다.

여기에는 선배 개발자 세션에서 오마이트립 CTO로 계신  [이규원](https://justhackem.wordpress.com/) 님의 영향이 컸습니다.

> 잘 관리된 깃허브와 블로그가 아니라면 이력서에 쓰지 마세요. 

스스로 블로그가 잘 정리되어있었는지 생각을 해보는 계기가 되었습니다. 

지금까지 딱히 남에게 보여주기 위한 글이라기보다는 제 생각을 정리하는 글이 많았기에 이력서를 검토하시는 분의 기준으로는 정성이 부족한 포스팅이 감점 요소일 것이라는 생각도 조금 들긴 합니다. 우려도 조금 되고요.

그러나 **결국 블로그는 이대로 내버려 두려고 합니다. 잘못된 정보가 아닌 한 누군가에게는 도움이 될 것이라는 생각**에서입니다.

---

### 17.08.26 (토)
[개발자커리어 Young Community 연합세미나](https://onoffmix.com/event/108861)에 참여하였습니다. 

- 초반 강의 대부분은 주로 대학생들, 혹은 1~2년 차를 대상으로 해서 크게 와닿는 부분은 없었습니다.
- 그렇지만 선배 개발자분들의 이력서 피드백이라든지 사회를 보시는 분의 피드백은 큰 도움이 되었다. 이력서를 수정하고 블로그를 재정비해야겠다는 생각이 들었습니다.

강의를 마치고 친구와 강남에서 열리는 IT인들의 치맥 파티에 갔습니다. 원래는 정보라든지 이런 것을 얻으려고 갔는데 그냥 치맥만 실컷 먹고 돌아왔습니다 (..)

---

### 17.08.25 (금)

#### MongoDB 
Replica set에 대한 개념을 알아보았습니다. [이곳](https://unagi44.wordpress.com/2015/09/10/mongodb-replica-set%EC%9D%98-%ED%95%84%EC%9A%94%EC%84%B1-3/)에 설명이 참 잘 되어 있었습니다.

#### Spring Boot
Spring Boot와 JRebel 연동이 제대로 안되는 현상을 [해결](http://jhleed.tistory.com/96)하였습니다.

[IntelliJ에서 Spring Boot를 생성하는 기능](http://blog.saltfactory.net/creating-springboot-project-in-intellij/)이 참 잘 되어 있다고 생각했습니다. 
생성부터 기본적으로 필요한 플러그인 (롬복 등..)을 한번에 가져와줍니다.

Spring Boot의 생산성을 직접 체험했습니다. 
게다가 `IntelliJ`와 같은 Idea를 쓰면 `application.property`에 자동완성까지 지원해줍니다.
토이 프로젝트라던지, 외주를 처리할때는 스프링 부트를 쓰면 **구현에 드는 시간이 확 줄어들 것 같습니다.**
