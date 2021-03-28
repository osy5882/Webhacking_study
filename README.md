# Webhacking_study

## 웹 기초 지식

### Web Browser
- 웹에 접속하기 위해 사용하는 '소프트웨어'
- 사용자가 웹과 HTTP의 동작 원리를 알지 못해도 웹을 사용할 수 있게 해줌.
### Web Resource
- 웹에서 사용하는 콘텐츠
- 사용자가 웹 브라우저를 통해 보게 되는 페이지를 구성하는 대표적인 웹 리소스로 HTML, CSS, JavaScript 등이 있음
  - HTML: 웹 문서의 뼈대를 구축하기 위한 마크업 언어
  - CSS: HTML이 표시되는 방법을 정의하는 스타일 시트 언어
  - JS: 페이지 내의 행위 설정
### URI(Uniform Resource Identifier)
- 리소스를 식별하기 위한 식별자
- 웹에 접속할 때 웹사이트의 주소를 이용해 접근할 때 사용
### Encoding
- 문자 또는 기호 등의 정보나 형태를 표준화, 보안 등의 목적으로 다른 형태나 형식으로 변환하는 처리 혹은 그 처리방식.
- 대표적인 인코딩은 URL Encoding과 HTML Entity Encoding이 있음.
  - URL Encoding: URL구조 내에서 예약어(구분어)로 사용하는 문자들을 전송하고자 할 때 사용/Ascii테이블의 Hex값 앞에 % 붙이면 됨.
  - HTML Entity Encoding: HTML 문서 내에서 사용하는 문자열들이 HTML에서 사용하는 태그로 인식하지 않도록 하기 위해 사용/ Ascii테이블의 Hex값 앞에 &#x 붙이면 됨.
### HTTP
- URI의 구성 요소 중 프로토콜(컴퓨터 사이에서 데이터를 교환하기 위한 규칙)에 해당.
- TCP(혹은 TLS)를 사용해 통신. 기본포트는 80(TLS는 443)
- 사용자가 서버에 요청하는 Request, 사용자의 요청에 대한 서버의 응답인 Respose로 나누어짐.
### HTTP Request
- 서버에 대한 요청.
- 첫 줄은 Method(수행하고자 하는 동작), Path(경로), Version(버전)으로 구성됨. 두 번째 줄부터는 Header부분. 나머지는 사용자의 데이터를 담는 Body가 있음.
### HTTP Response
- 사용자의 요청에 대한 서버의 응답.
- 첫 줄은 Version과 Status Code(사용자의 요청에 대한 서버의 상태응답코드)로 구성됨/이후는 위와 동일.
- Status Code
  - 200번 영역: 서버 처리 성공
  - 300번 영역: 요청 리소스가 다른 경로로 변경됨
  - 400번 영역: 요청 구조 또는 데이터가 잘못됨
  - 500번 영역: 서버의 에러와 관련
### Cookie
- connectionless, stateless 프로토콜을 사용하면 하나의 Request에 하나의 Response를 한 후 네트워크 연결을 끊고 이 때 상태를 유지하지 않음. 따라서 HTTP 요청마다 새로운 커넥션을 열고 사용자 인증을 계속해서 해야함. 이를 개선하기 위해 Cookie가 탄생함.
- 사용자 인증을 계속 하지 않기 위해 그 데이터를 쿠키에 저장하고 추후 HTTP 요청을 보낼 때 웹 브라우저가 자동으로 헤더에 쿠키를 추가해 전송함.
### Session
- 쿠키에 인증상태를 포함한 데이터를 저장 가능. 
- 쿠키에 인증 상태를 포함한 데이터를 저장하면 사용자가 임의 사용자로 인증되 넋 처럼 요청을 조작할 수 있음. 따라서 서버에 데이터를 저장하기 Session을 사용.
### HTTP/HTTPS
- HTTP는 암호화 되지 않은 평문으로 전송.
- HTTPS는 공개키 암호화를 사용하여 데이터들을 암호화 하여 전송.
### Domain Name/Host Name
- IP는 네트워크 통신 시 장치를 식별하기 위한 주소임. 이는 불규칙적인 숫자로 이루어져 있기 때문에, 사람이 외우기 쉽고 의미를 부여하기 위해 Domain name을 사용.
- Domain Name은 DNS에 저장되어있고 DNS를 조회해 등록된 IP 주소를 가져와 사용.
