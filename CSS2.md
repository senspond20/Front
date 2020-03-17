
```html
※

-------기초선택자--------------------------------------------------------------------------------------------
※기본형
*{ ;} : 모든선택자
p{ ;} : p태그 적용
#id{ ;} : id적용
.class{ ;} : class적용
- 속성 선택자
div[name=name1] : name이 name1인 거 적용
div[name~=name1] : name이 name1이 들어가고 공백으로 구분되는 거
div[name|=name1] : name이 name1이 들어가고 -로 구분되는거
div[class$=class] : class가 class로 끝나는
div[class*=v-c] : class가 v-c가 포함되는 거
- 자손/후손 선택자
#testDIv>h4 : 자손 선택자, 앞id 범위의 바로 아래 모든 h4요소, 더 안쪽에 있는건 한번 더 들어가야함(ex)#testDiv>ul>li
#testDiv li : 후손 선택자, 앞id범위에서 모든 li요소
- 동위 선택자
#div-test2+div{ ;} : div-test2 뒤에 div하나에 적용
#div-test3~div{ ;} : div-test3 뒤에 모든 div에 적용
- 반응 선택자
#active-test:active{ ;} : active-test를 마우스로 클릭 시 적용
#hover-test:hover{ ;} : hover-test를 마우스 댈 시 적용
- 상태 선택자
input[type="checkbox"]:checked{ ;} : input태그에 type이 checkbox인 것 체크표시시 적용
#userId:focus{ ;} : userId에 커서가 있을 시 적용
- select에서 선택 불가능한 option변경
option:disabled{ ;} : option태그 중 선택불가 인거에 적용
option:enabled{ ;} : option태그 중 선택가능 인거에 적용
- 일반 구조 선택자 : 위치 후 태그
#test1 p:first-child{ ;} : test1안의 첫 번째가 p일 시 적용
#test1 p:last-child{ ;} : test1안의 마지막이 p일 시 적용
#test1 pre:last-child{ ;} : test1안의 마지막이 pre일 시 적용
#test1 p:nth-child(2n){ ;} : test1안의 2의 배수 번째가 p일 시 적용
#test1 p:nth-last-child(4n){ ;} : test1안의 뒤에서 태그 4의 배수가 p일 시 적용
- 형태 구조 선택자 : 태그 후 위치
#test2 p:first-of-type{ ;} : test2안의 p태그 첫번째 적용
#test2 p:last-of-type{ ;} : test2안의 p태그 마지막 적용
#test2 p:nth-of-type(2n){ ;} : test2안의 p태그 2의 배수인 거에 적용
#test2 p:nth-last-of-type(4) : tset2안의 뒤에서 p가 4번째 인거에 적용
- 문자 선택자
#test3 p : first-letter{ ;} : test3안 p의 첫 글자에 적용
	first-line{ ;} : test3안 p의 첫 번째 줄에 적용
	after{content:" " ;} : 태그 뒤에 내용 추가
	before{content:" " ;} : 태그 앞에 내용 추가
	selection{ ;} : 드래그 한 글자
1)background
2)color
3)width, height
4)cursor
5)font-size
6)content
-------텍스트 스타일--------------------------------------------------------------------------------------------
1)font-family: 궁서체 | 굴림체 |     *여러 개 쓸 시 있는 글꼴 나올 때까지 뒤로감 없을 시 기본글꼴
2)font-size: px | em | %
3)font-weight: bold | lighter | 900
4)font-variant: small-caps → 작은 대문자
5)font-style: italic | oblique → 기울임
6)font: style variant weight size/line-height family     * line-height : 라인 공백
7)color: 색상영문이름 | 16진수 숫자 | rgb(N,N,N) | rgba(N,N,N,0.N) | hsl(N,N%, N%) | hsla(N,N%,N%,0.N)
8)text-decoration: none | underline | line-through | overline
9)text-transform: none | capitalize | uppercase | lowercase   * capitalize : 첫 글자마다 대문자
10)text-shadow: px px px 색깔
11)white-space: normal | nowrap | pre | pre-line | pre-wrap
a.normal: 모든 공백을 하나공백으로 처리
b.nowrap: 모든 공백을 하나공백으로 처리 후 한줄로 표현
c.pre: pre화
d.pre-line : 모든 공백을 하나공백으로 처리, 줄바꿈은 적용, 창에 크기에 따라 자동 줄바꿈
e.pre-wrap : pre화, 창에 따라 자동 줄바꿈
12)letter-spacing: px  → 글자마다의 공백간격
13)word-spacing: px  → 단어마다의 공백간격
14)direction: ltr | rtl  → 글자쓰기 방향
15)text-align: left | right | center | justify   *justify: 양쪽 정렬
16)text-indent: px   → 문장 들여쓰기
17)line-height: normal | px → 줄바꿈 간격
18)overflow: hidden   → 영역 벗어나는 텍스트 숨기기
19)text-overflow : clip | ellipsis → clip 아무것도x, ellipsis: overflow부분부터 ...으로 표현
20)list-style-type: disc | circle | square | none / decimal | decimal-leading-zero | lower-roman | upper-roman | lower-alpha | upperalpha
-------색상 스타일----------------------------------------------------------------------------------------------
1)background-color:   → 배경 색
2)background-clip: border-box | padding-box | content-box
a.border-box : 경계선 포함
b.padding-box : 경계선 제외
c.content-box : 내용만 포함
3)background-image: url(' ')   → 배경으로 이미지 넣을 때
4)background-repeat: repeat | repeat-x | repeat-y | no-repeat
5)background-size: auto | contain | cover | 150px 100px | 80% 80%
6)background-position: left top | right top | center top | left bottom | right bottom | center bottom |left center | right center | center center
			| 30px 50px | 50% 50%
7)background-origin: border-box | padding-box | content-box
8)background-attachment: scroll | fixed
-------레이 아웃 스타일----------------------------------------------------------------------------------------------
- 화면 배치 방법
1)border: 1px solid|dashed black;
2)display: inline | inline-block | block | none(없어짐)
- 테두리 스타일
3)border-style: none | hidden | dotted | dashed | double | groove | inset | outset | ridge | solid
4)box-shadow: 수평 수직 흐림 번짐 색
5)border-top-color: red;   → 위 경계선 색
6)border-color: red   
7)border-bottom-right-radius: 50px
8)border-width: px   → 경계선 두꼐
- 여백 스타일
9)padding | padding-top | padding left: px
10)margin | maring-top | margin-left : px
* padding은 영역 안에서의 여백확보, margin은 영역 밖에서의 여백확보
- 포지셔닝
11)position: relative | absolute | fixed     → 상대 위치 영역들은 절대위치 순으로 뒤에 위치, fixed 고정위치(일찍 적어야 보임)
12) top: px; left: px;   → 위치 지정
13)visibility: hidden   → 속성 적용 안보이게함 공간만 보임
14)z-index : 클수록 위에 위치
15)float : left | right   → 왼쪽부터 채우거나 오른쪽부터 채움
- 다단 스타일
16)column-width: px  → 단 너비
17)column-gap: px  → 단 사이의 간격
18)overflow: scroll   → overflow범위 scroll로
19)column-count: N  → 단 객수
20)column-rule-style: dashed; → 단 경계선
21)column-rule-color: red;   → 단 경계선 색
22)#column2>h5{column-span: all;}    → h5 이하 문장을 h5아래로 가게함
- 표 스타일
23)caption-side:
24)border-collapse: collapse | seperate;  → collapse: 한줄 선으로 만듬, table경계선 없어짐, seperate: 기본, 두줄
25)border-spacing: px px   → 칸마다 간격
26)empty-cells: hide   → 빈칸 숨기기
27)table-layout: fixed → 글자수 상관없이 너비높이를 설정값으로
28)word-break: break-all;   → 글자수만큼 높이만 늘어남
29)vertical-align: top   → 글자가 칸 위쪽에 배치
-------변형----------------------------------------------------------------------------------------------------
#id:hover{ }
1)transform: translateX(px) | translateY(px) | translate(px, px)
2)transform: scaleX(2) | scaleY(2) | scale(2, 2)
3)transform: rotate(45deg)
4)transform: skewX(45deg) | skewY(45deg) | skew(deg, deg)  →뒤틀기
5)transfrom: perspective(300px)  → z축으로 확장
	    translate3d(px, px, px) | translateZ(px) | rotateX | rotateY | rotateZ | rotate3d(2.5, 1.5, 1.5, 30deg)
6)transform-origin: left top | right top | left bottom | right bottom
7)backface-visibility:hidden   → 회전하여 뒷면 보일 시 사라짐

```