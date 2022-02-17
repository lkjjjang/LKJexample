스프링 레거시 기반 설정 모음
폼파일은 필요에 따라 디펜더시 추가
root, servlet context 는 폴더 경로 확인후 작업
web.xml 한글 인코딩 포함되어 있음 전자정부는 한글인코딩 되어있으니 필요에 따라 사용
설정파일 순서

모든 동작은 interface 기반 실제 구현체만 넘겨 줌으로 개체 또는 로직 변경이 쉽다.
controller 에서 사용 되는 개체생성 순서
1. 최초 설정파일 root-context에서 정의된 설정을 읽어 개체 생성
2. dao에 Autowired, Inject 사용해서 주입
3. service에 Autowired, Inject 사용해서 주입
4. controller에 Autowired, Inject 사용해서 주입


기본 경로

|-- src
|    |-- main
|        |-- webapp
|            |-- MATA-INF
|            |-- resources
|            |-- WEB-INF
|                |-- lib 
|                |-- spring
|                    |-- appServlet
|                        |-- servlet-context.xml
|                    |-- root-context.xml
|                |-- views
|                    |-- 페이지보관
|            |-- web.xml

