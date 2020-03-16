# HTML5

-구조적 설계 지원(시멘틱)
-그래픽 및 멀티미디어 기능 강화
- CSS3 및 Javascript 지원
- 다양한 API 제공
- 모바일 웹 지원 및 장치 접근 가능(배터리 정보, 카메라, GPS 등)
- 웹 브라우저가 서버와 양방향 통신 가능
- 인터넷이 연결되지 않은 상태에서도 애플리케이션 동작

※ 주의 사항
- 태그는 대/ 소문자를 구분하지 않으나 소문자를 권장함
- 시작 태그로 시작하면 반드시 종료 태그로 종료
- 파일 확장자는 반드시 html 또는 htm 으로 설정
- 문자의 공백은 몇 개를 입력하든 한 개만 인식하므로
  공백을 추가하기 위해서 특수기호 &nbsp; 를 이용해야 함

※ 기본형태
```html
	<!doctype html>
	<html> 
	<head>
			<title>페이지 제목 </title>
		</head>
		<body>
		</body>
	</html>
```
--------------------
# 태그 정리

+ ## 글자관련

	```html
	1)<!-- -->: 주석
	2)&nbsp; : 띄어쓰기
	3)<hn> </hn> : 부 제목
	4)<br> : 줄 바꾸기
	5)<hr> : 가로로 밑줄을 만들어줄 때
	6)&lt &gt : < >
	7)<strong></strong>, <b></b> : 굵게 만들기
	8)<mark></mark> : 형광펜 효과
	9)<u> </u> : 밑줄
	10)<s> </s> : 취소선
	11)<em> </em>, <i> </i> : 기울임
	12)<small> </small> : 작은 글씨
	13)<blockquote> </blockquote> : 들여쓰기 인용문구
	14)<q> </q> : "" 인용문구
	15)<sub> </sub> : 아래 첨자
	16)<sup> </sup> : 윗 첨자
	17)<abbr title=""> </abbr> : 마우스 올릴 시 추가설명
	18)<cite> </cite> : 강조기울임(ex)영화제목)
	19)<code> </code> : 얇은 글씨, 코드보여줄 때 사용
	20)<pre> </pre> : 들여 쓰기, 띄어쓰기 그대로 출력
	21)<p> : 단락만 구분, 띄어쓰기하나씩 적용
	```


+ ## 목록관련
	```html
	1)<ul> <li> </li>~ </ul> : 불릿 목록, 들여쓰면 모양 바뀜
	2)<ol> <li> </li>~ </ol> : 순서 있는 목록, 들여써도 같음 1. 2.~~
	a.<ol type = ""> : 영문 소문자(a), 영문 대문자(A), 로마 숫자 소문자(i), 로마 숫자 대문자(I)
	b.<ol start= ""> : 숫자만 입력가능 시작 값 변경하기
	c.reversed="reversed"> : 역순으로 표시
	3)<dl> <dt> </dt> <dd> <dd>~ </dl> : 설명 목록, dt는 제목, dd는 설명(들여쓰기 되서 들어감) 여러 개 가능
	```

+ ## 표관련

	```html
	※기본 형태
	<table border='1'> 
	<caption> </caption>
		<tr>
			<th> </th>
		</tr>
		<tr>
			<td> </td>
		</tr>
	</table>
	<figure>
		<figcaption></figcaption>
	</figure>
	1)<table> </table> : 표 형태
	2)<tr> </tr> : 행을 나눔
	3)<td> </td> : 열을 나눔
	a. width : 너비설정
	b. height : 높이 설정
	c. rowspan : 행 병합
	d. colspan : 열 병합
	4)<th> </th> : 열에 대한 제목을 표시, 중앙정렬 및 굵게 표시
	5)<caption> </caption> : 테이블 제목
	6)<figure> <figcaption></figcaption> </figure> : 테이블 설명, img의 설명, figcaption하나당 들여쓰기 후 한줄 
	7) <thead><thead> <tbody> </tbody>~ <tfoot> </tfoot> : 표 영역을 나누고, 스타일 적용도 가능
	8) <col>, <colgroup> </colgroup> : table태그 바로 뒤에 들어가서 열에 대한 스타일 적용 시 사용, 후자는 그룹으로 묶어 적용
	```

+ ## 영역관련

	```html
	1)<div> </div> : 위에서 아래로 영역넓힘, 블럭요소
	a.style="border: 1px solid black; : 1크기테두리 검정네모
	b.width, height
	c.background : 바탕 색
	d.color : 글자 색
	2)<span> </span> : 좌에서 우로 영역넓힘, 인라인요소, 크기지정 불가
	a.style="border: 1px solid black; : 1크기테두리 검정네모
	b.background
	c.color
	3)<ifame> </iframe> : 웹 문서 안에 다른 웹 페이지를 추가하는 태그
	a.width, height
	b.src

	* 시맨틱 태그 : 인라인 요소들
	4)<header> </header> : 머리말, 검색어, 메뉴
	5)<nav> </nav> : 태그모음, footer에 자주사용
	6)<section> </section> : 콘텐츠 주제
	7)<article> </article> : 콘텐츠 내용, 여러개
	8)<aside> </aside> : 광고 삽입
	9)<footer> </footer> : 회사 소개, 저작권
	```

+ ## 멀티미디어관련

	```html
	1)<img> </img> : 이미지
	a.src=""
	b.alt="" : 이미지 설명
	c.width, height
	d.usemap="#~" : map태그를 쓰기위한 맵이름
	2)<map name=""><area> </area> </map> : 
	a.shape="rect" : 사각형모양
	b.coords="0, 0, 300, 500" : 사진의 (0.0)위치부터 너비300 높이500범위
	c.href="" : 링크
	d.target="_self" : 현재 페이지이동, _blank는 새 페이지
	3)<audio> </audio> : 오디오
	a.src=""
	b.autoplay : 자동 재생
	c.controls : 컨트롤러
	d.loop : 반복
	4)<video> </video> : 비디오
	a.src=""
	b.controls
	c.preload="auto | metadata | none" : 미리 다운로드 | 기본정보만 가져옴 | 미리 다운로드x
	d.autoplay
	e.loop
	하이퍼링크관련
	1)<a> </a> : 하이퍼 링크
	a.href="링크 | #id" : id위치로 이동가능
	b.target="_blank | _self | iframe의name | #id" : iframe 안에 이미지불러오기 가능
	```

+ ## 폼관련

	```html
	1)<form> </form> : 폼
	a. action="" : 전송 받을 서버의 클래스명
	b. method="get | post" : 기본값 get URL창에 보임, post는 안보임
	c.name
	d. target= : 페이지를 어떻게 열지
	e.autocomplete : 이전 입력내용 출력
	2)<input> : 박스칸
	a.type="text : 입력칸
	| submit : 전송버튼
	| hidden : 안보이고 전송가능
	| password : 불릿기호로됨
	| button : 단순 버튼
	| reset : 취소
	| radio : 하나만 선택하는 칸, name을 같게해야 적용됨, checked속성 추가 시 찍혀있음
	| checkbox : 여러개 선택할 때, name을 같게 해야함
	| file : 파일 선택하여 표시 가능, multiple 속성을 추가하여 여러 파일 선택가능, accept=".jpg, .PNG"로 jpg png파일만 선택가능
	| image : 이미지를 버튼으로 클릭한 x,y좌표를 전송
	| search : 검색 칸
	| url : 홈페이지(http://로 시작해야함),value="http://"하면 유용
	| email : ~@~형태 여야함
	| tel : 전화번호 칸
	| number :  숫자 입력, min max value step 정할 수 있음
	| range : 슬라이드바, min max step 정할 수 있음
	| data : 연도 월 일
	| month : 년 월 
	| week : 년 번째 주 
	| time : 오전|오후 시 분
	| datatime : 직접 적기, 거의 안씀
	| color : 색상 선택
	b.name
	c.placeholder="" : 쓰기 설명
	d.size="" : 박스칸 너비
	e.maxlength="" : 글자 수 제한
	f.value="" : 미리 텍스트창에 채울 글자
	g.autofocus : 웹페이지 시작 시 커서위치함
	h.readonly : 읽기 전용, 수정 불가
	i. value : 전송값이나 버튼의 이름
	2)<fieldset> <legend> </legend> </fieldset> : 필드셋, legend에 제목작성
	3)<label> </label> : 따로 이 영역을 관리하기 위한 표시
	4)<button> </button> : input의 button, submit, reset을 만들 수 있음
	a.type="button | submit | reset" : form태그 안에서는 기본값이 submit으로 됨
	5)<select name="" size="" (multiple)> <option> </option> </select> : 선택바
	a.value
	b.selected : 먼저 나오기
	6)<textarea> </textarea> : 큰 입력 창
	a.cols rows : 행렬 크기
	b.style="resize: none;" : 크기 변경 불가, 기본값은 크기변경 가능
	```