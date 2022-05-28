# APM
1. apache
2. php
3. mySql

장점: 무료

## 1. Apache
```
key : html, php, web server
1995년 처음 발표된 WWW(월드 와이드 웹) 서버용 소프트웨어이다.
'A Patch server'라는 용어에서 아파치라는 이름을 따왔다.
오픈소스 라이선스에 따라 무료로 배포되어 원하는 사람들이 자유롭게 사용할 수 있다.
유닉스, 윈도우 등 거의 모든 운영체제와 시스템에서 운용이 가능하다.

아파치 소프트웨어 재단이라는 단체가 오픈소스 프로젝트의 아파치 커뮤니티를 지원하고 있다.
```

### * Apach Tomcat
```
key : jsp, java servlet, was server
아파치 소프트웨어 재단(Apache Software Foundation)에서 개발된 서블릿 컨테이너(웹 컨테이너)만 있는 웹 애플리케이션 서버이다.
톰캣은 웹 서버와 연동하여 실행할 수 있는 자바 환경을 제공하여 자바 JSP(자바 서버 페이지)와 자바 서블릿이 실행할 수 있는 환경을 제공하고 있다.
톰캣은 관리툴을 통해 설정을 변경할 수 있지만, XML 파일을 편집하여 설정할 수도 있다.

아파치 톰갯에 내장된 웹 서버로만 웹 시스템을 구성할 수 있지만, 대규모의 사용자가 사용하는 시스템을 구축하려면 웹 서버와 연동하는 안정적인 시스템을 구축해야 한다.

톰캣은 html 같은 정적 페이지를 로딩하는데 웹 서버보다 수행 속도가 느리다.
이를 해결하기 위해서 아파치와 연동한다. 아파치가 실행되면 아파치는 html 파일은 자신이 수행하고 jsp 파일은 톰캣으로 넘겨서 톰캣이 수행하게 만든다.
톰캣 특성상 java 언어만 해석이 가능하기 때문에 톰캣에 자체 내장되어 있는 http 서버를 사용하더라도 php언어로 작성된 서버 페이지는 실행이 불가능하다.
따라서 아파치에서 php를 호출하고 톰캣에서 jsp를 호출하도록 상호 보완적 구조를 구성할 수도 있다.
```

### * Difference
```
웹 컨테이너 기능의 차이(동적 통신)
클라이언트의 요청이 있을 때 내부의 프로그램을 통해 결과를 클라이언트(사용자의 PC 브라우저)에 전달해주는 역할

웹 서버는 클라이언트의 요청에 매번 웹페이지로 응답한다. 페이지가 계속 새로고침된다.

웹 어플리케이션 서버는 클라이언트의 요청에 데이터를 응답한다. 페이지의 일부가 변경된다.
```

## 2. PHP
```
인터넷이 보급 초기에는 Perl언어와 C언어를 가지고 웹사이트를 제작했다.
하나의 클라이언트에 하나의 프로세서를 생성했다.
그리고 더 효율적인이고 다양한 웹 언어가 개발되었다.
- 마이크로소프트의 ASP
- SUN의 JSP
- ZEND의 PHP
위 셋이 대표적인 웹 언어였다.
하나의 클라이언트에 하나의 프로세서를 만든 후 하나의 쓰레드를 생성하여 쓰레드 단위로 요청을 처리해서
서버에 부담을 줄였다.

PHP모듈 C언어로 개발되어 문법이 C와 비슷하고 실행속도 또한 빠르다.

PHP는 초기에 한 개인에 의해 개발되어 오픈소스화되어 유명해진 웹언어다
Apache 웹서버와 연동하여 동작한다.

```