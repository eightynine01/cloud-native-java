6장 REST API
===

2018-07-17, 박태환(eightynine01@gmail.com)

---
* 레너드 리차드슨의 성숙도 모델
* 컨텐트 협상(Content negotiation)
* 하이퍼미디어(Hypermedia)
* 구글프로토콜
* ~~REST API 문서화~~

---
## 레너드 리차드슨의 성숙도 모델

### Level 0
* 일반 XML(POX, Plain Old XML) 데이터를 SOAP이나 XML-RPC 등으로 전송한다. POST 메소드만 사용하며, 서비스 간에 단일 POST 메소드로 XML 데이터를 교환한다. 초창기 SOA 애플리케이션 제작 시 흔히 사용된 방식이다.
### Level 1
 * 자원 형태로 구분되어 있으나 액션을 CRUD (Create, Read, Update, Delete)로 표현하지 않은 HTTP API
### Level 2
 * 자원 형태와 액션 등의 URI가 구분지어 있는 REST API
### Level 3 (HATEOAS)
 * response payload 에 관련 URI를 포함하는 Hypermedia 로써의 속성을 지님으로써 Code on demand 속성을 지원할 수 있는 완전한 REST API


---
## 컨텐트 협상(Content negotiation)

* https://code-examples.net/ko/docs/http/content_negotiation

---
## 하이퍼미디어(Hypermedia)

* 잘 동작하는 API를 제대로 사용하려면 클라이언트는 어느 종단점을 호출해야 하는지 언제, 어떤 메소드로 호출해야 하는지 알아야 한다.
* HTTP OPTIONS 메소드를 활용하면 요청하려는 자원을 어떤 메소드로 접근 할 수 있는지 알 수 있다.
* 모든 자원 요청에 대해 현재 서비스에 의해 만들어진 최신 링크 정보를 포함해서 클라이언트에게 반환하면, 클라이언트는 그 최신 링크를 통해 항상 서비스의 최신 상태에 맞는 정보를 얻을 수 있다고 주장한다.

---
## API 버저닝

* 모든것은 변한다
* 자기가 만들어내는 것에는 보수적이어야 하지만 다른 서비스를 받는 것에는 관대해야함
-- [견고함 원칙](https://en.wikipedia.org/wiki/Robustness_principle)
* 시맨틱 버저닝(semantic versioning)
-- 메이저, 마이너, 패치 형식을
---
## ~~REST API 문서화~~

---
## 클라이언트

* 파이어폭스의 포스터 플러그인 (https://code.google.com/archive/p/poster-extension/)
* cURL (https://curl.haxx.se/)
* HTTPie (https://httpie.org/)
* Postman (https://www.getpostman.com/)
