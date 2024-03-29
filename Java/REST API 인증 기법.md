# REST API 인증 기법
인증 서버의 스케일 한계를 해결하기 위한 인증 기법은 무엇일까?

## 1. Basic 인증
상태가 없는 웹 애플리케이션에서 인증을 구현하는 가장 간단한 방법은 무엇일까?
가장 간단한 방법은 모든 HTTP 요청에 아이디와 비밀번호를 같이 보내는 것이다.
이런 방법을 basic 인증이라고 한다.  
basic  인증에서는 최초 로그인한 후 http 요청 헤더의 authorization 부분에
Basic <ID>:<Password> 처럼 아이디와 비밀번호를 콜론으로 이어붙인 후 
Base64로 인코딩한 문자열을 함께 보낸다.


__Authoriztion: Basic aGVsbG93b3JsZEBnbWFpbC5jb206MTIzNA==__  


문제점.. 인코딩은 보안을 목적으로 하는 것이 아니다.
육안으로 아이디와 비밀번호를 찾아내기 힘들지만 디코더만 있다면 누구나 디코딩해 원래의
아이디와 비밀번호를 확인할 수 있다.  
또한 이 솔루션을 이용하면 사용자를 로그아웃시킬 수 없다.
모든 요청이 일종의 로그인 요청이기 때문이다.  
인증 서버와 인증 DB에 과부하가 걸릴 확률이 높다. 
규모가 작은 애플리케이션의 셩우 굳이 스케일에 대해 고민할 필요가 없다.
그러나 마이크로서비스 기반의 어플리케이션 구조에서는 서비스의 개수만큼 인증 서버가 호출되므로
비효율적이다.    


## 2. 토큰 기반 인증 / Bearer 인증
토큰은 사용자를 구혈할 수 있는 문자열이다.
토큰은 최초 로그인 시 서버가 만들어 준다. 서버가 자기만의 노하우로 토큰을 만들어 반환하면
클라이언트는 이후 요청에 아이디와 비밀번호 대신 토큰을 계속 넘겨 자신이 인증된 사용자임을 알리는 것이다.  


__Authoriztion: Bearer aGVsbG93b3JsZEBnbWFpbC5jb206MTIzNA==__ 


토큰을 기반으로 하는 요청은 헤더에 Autoriztion: Bearer <TOKEN>을 명시한다.  
Basic 인증 기법보다 보안 측면에서 좀 더 안전하다.
또 서버가 토큰을 마음대로 생성할 수 있으므로 사용자의 인가정보 또는 유효 시간을 정해 관리할 수 있다. 하지만 Basic 인증에서 마주한 스케일 문제를 해결하지는 못한다.    


## 3. JSON 웹 토근 
서버에서 **전자 서명된 토큰**을 이용하면 이증에 따른 스케일 문제를 해결할 수 있다.
JWT는 JSON 형태로 된 토큰이다. 


JWT 토큰은 아래의 요소로 구성된다.
{header}.{payload}.{signature}
__Authoriztion: Bearer aGVsbG93b3Js.ZEBnbWFpbC5jb.206MTIzNA==__ 


[디코딩한 JWT 예]  
```  
{
	"typ" : "JWT",
	"alg" : "HS512"  
}.  
{
	"sub" : "5243523524c3453425",
	"iss" : "demo app",
	"iat" : 123451214,
	"exp" : 123451214
}.  
NqwerjwekrnKLNKL343234234234ADS
```


```
전자 서명이란 {헤더}, {페이로드}와 시크릿키를 이용해 해시 함수에 돌린 암호화한 결과 값이다.
시크릿키란 나만 알고 있는 문자열, 비밀번호 같은 것으로 서버가 가지고 있다.
인증 서버에 토큰의 유효성에 대해 물어볼 필요가 없다.
이는 인증 서버에 부하를 일으키지 않는다는 뜻이고 더 이상 인증 서버가 단일 장애점이 아니라는 뜻이기도 하다.
```


### 서버의 전자서명 생성
최초 로그인 시 서버는 사용자의 아이디와 비밀번호를 서버에 저장된 아이디와 비밀번호에 비교해 인증한다. 사용자의 정보를 이용해 {헤더},{페이로드} 부분을 작성하고 자신의 시크릿키로 {헤더},{페이로드} 부분을 전자 서명한다. 전자 서명의 결과로 나온 값을 {헤더},{페이로드}.{전자서명 결과}으로 이어붙이고 Base64로 인코딩한 후 반환한다.


### 인증
위에서 생성된 토큰으로 리소스 접근을 요청하면 서버는 일단 이 토큰을 Base64로 디코딩한다.
서버는 {헤더}.{페이로드}와 자신이 갖고 있는 Secret key로 전자 서명을 만든 후 http 요청이 갖고온 {서명} 부분과 비교해 이 토큰의 유효성을 검사한다.


### 다음 내용 > 스프링 시큐리티 통합

