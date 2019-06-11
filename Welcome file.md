
# 1. 주제선정


## 1) 스트리밍 플레이어

<스트리밍>

멜론지니벅스st
지니에 쫌더 가깝게!

아직 이해가 살짝 안됨...
지니같은 사이트를 만드는데 지니에 있는 음악 데이터들을 가져와서 사용??약간 중간다리역할??

음악에대한 단순한 정보는 웹크롤링으로 가져올수있을거같은데
지니서버,디비에접속해서 음악자체를 가져와 재생까지 시킬수있는건징...?



진석오빠가 올려줬던 깃헙 링크 많이많이 참고

직캠영상등은 유튜브에서 따오는걸로!

노래자랑영상은 유튜브랑 연동해서 올릴것인지 아니면 그냥 사이트내에서만 볼수있게??



### Development Environment

-   IDE : STS (Spring Tool Suite) 3.8.1.RELEASE
-   WAS : Tomcat 8.5
-   OS : Window8 (64 bit)
-   Language : Java 1.8, HTML, CSS, Javascript, JQuery
-   DB : Oracle 
-   Persistence Framework : MyBatis

### 기능

1. **플레이어**
2. **로그인**
3. **차트**
4. 리스트
5. 좋아요
6. 게시판
7. 실시간 채팅
8. 직캠영상
 
### 참고자료

- [음악 검색 및 스트리밍 서비스](https://github.com/kinayoon/Music-Searching-and-Streaming)
- [napster API - 플레이어 api](https://developer.napster.com/)
- [ㄴnapster Example](https://jsfiddle.net/napstercat/c4zczg6j/?utm_source=website&utm_medium=embed&utm_campaign=c4zczg6j)

## 2) 영화

<영화통합>
공통사항
서버, 디비, 개발툴 등등 어떤걸 사용할지?



삐끼라는 앱이 있는데 3사통합해서 예매정보?예매오픈했는지 알려줌, 아이폰안드웹다됨!

데이터는 웹크롤링으로 다 긁어올 수 있을듯
모든 영화에 대한 정보는 공공디비에서 가져올수있음

게시판은 그냥 스프링 마이바티스 등등 사용

로그인은 구글 페이스북 카톡등등 오픈api사용
스프링 시큐리티같은걸로 직접 구현하는것도 큰 도움이 될듯! 
모든 개인정보(이메일주소, 전화번호 등)는 개인정보보호를 위해 최대한 꽁꽁숨겨놓기!

포인트적립은 어떤식으로 제공할지..?
글작성시 몇포인트 적립 이런식으로...?
근데 씨집롯시메박의 정보를 긁어와서 뿌려주는건데 
자체만의 리뷰같은걸 받는게 좋을지...?




### Development Environment


-   IDE : STS (Spring Tool Suite) 3.8.1.RELEASE
-   WAS : Tomcat 8.5
-   OS : Window8 (64 bit)
-   Language : Java 1.8, HTML, CSS, Javascript, JQuery
-   DB : Oracle 
-   Persistence Framework : MyBatis


### 기능

1. CGV, 메가박스, 롯데시네마 등의 영화 정보 제공
2. 리뷰 모아오기
3. 예매
4. 매점 이용권 ( 중고장터)
5. 게시판
6. 포인트 정립
7. 나영리(나만의 영화 리스트)
8. 넷플, 왓챠


### 참고자료 - API 등
- [![KOBIS 영화관 입장권 통합 전산망](http://www.kobis.or.kr/kobis/web/comm/images/comm/logo_comm.png)](http://www.kobis.or.kr/kobis/business/mast/mvie/findOpenScheduleList.do)
- [ ![KOFIC](http://www.kobis.or.kr/kobisopenapi/web/images/common/logo.gif)  ![영화권입장권통합전산망 오픈API](http://www.kobis.or.kr/kobisopenapi/web/images/common/logo_sub.gif)](http://www.kobis.or.kr/kobisopenapi/homepg/apiservice/searchServiceInfo.do)
- [rapidapi - movie](https://rapidapi.com/collection/movie-apis)
- [웹 크롤링관련 - BeautifulSoup ](https://www.yceffort.kr/2018/11/05/web-crwaling-for-naver-movie/)

# 2. 형상관리

# 3. 협업툴

# 4. 서버

<!--stackedit_data:
eyJoaXN0b3J5IjpbLTE1OTg4NDI1ODVdfQ==
-->