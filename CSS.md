# CSS

```html
▶ style과 stylesheet

style은 정해진 속성을 입력하여 웹 페이지를 꾸미는 것 stylesheet는 웹 페이지에서 반복적으로 쓰는 style을 모아놓은 것

문서 내용 작성과 꾸미는 부분을 분리하여 내용을 수정해도 디자인을 바꿀 필요가 없고 디자인을 수정해도 글 내용을 바꿀 필요가 없음 다양한 기기에도 디자인만 따로 적용하여 구동시킬 수 있음
p{text-align: center;}

▶ CSS 적용 

 내부 스타일 시트
<style></style> 내부에 스타일 정보를 저장하는 방법
<style>
p{text-align: center;}
</style>

 외부 스타일 시트
<link>태그를 이용하여 css파일을 읽어와서 스타일 적용
<link href=“css 파일 경로“ rel=“stylesheet” type=“text/css”>
```


▶ CSS 선택자

전체 선택자/태그 선택자
아이디/클래스 선택자
기본 속성 선택자
문자열 속성 선택자
후손 선택자/자손 선택자
|구분 | 내용
|:---:| ----
|전체 선택자 |* 
|태그 선택자 |태그(h1, p, li 등) 
|아이디 선택자 |#아이디명 
|클래스 선택자 |.클래스명 
|후손 선택자| 선택자 선택자 
|자손 선택자|선택자 > 선택자
|속성 선택자| 선택자[속성```=```값] / 선택자[속성```~=```값] |
|          |선택자[속성```|=```값] / 선택자[속성```^=```값] |
|          |선택자[속성```$=```값] / 선택자[속성```*=```값]  |
|동위 선택자| 선택자 + 선택자 / 선택자 ~ 선택자
|구조 선택자| 선택자:first-child / 선택자:last-child 
|          |선택자:nth-child(수열) / 선택자:nth-last-child(수열) 
|          | 선택자:first-of-type / 선택자:last-of-type 
|          | 선택자:nth-of-type(수열) / 선택자:nth-last-of-type(수열) 
|반응 선택자|선택자:active / 선택자:hover
|상태 선택자|:checked / :focus :enabled / :disabled 
|링크 선택자| :link / visited
|문자 선택자|::first-letter / ::first-line ::after / ::before /::bselection 
|부정 선택자| 선택자:not(선택자)


```
▶ CSS 우선순위 
 +  적용 방법에 따른 순위

태그 스타일 > class 스타일 > id 스타일 > 인라인 스타일 > !important

 + 소스 순서에 따른 순위

나중에 작성된 스타일 적용
```

## 텍스트 스타일

+ 웹 폰트 제공사이트 : http://fonts.google.com

```html
<!-- 적용 -->
<head>
<link href="폰트URL" rel="stylesheet">

</head>
```

### § 글꼴 속성 

+ **font-family** : 선택자{font-family: 글꼴1[, 글꼴2, 글꼴3];}

    폰트의 글꼴을 설정해주는 속성으로 글꼴1이 없으면 글꼴2, 글꼴3으로 선택되어 설정됨, 다 없으면 브라우저 기본 글꼴로 적용

+ **font-size** : 선택자{font-size: 숫자단위;}

    글자의 크기를 조절하는 속성으로 em, px, pt 단위가 있음

+ **font-weight**
    글자 굵기를 조절하는 속성
    normal/bold/bolder/lighter/100~900

+ **font-variant** : 선택자{font-variant: normal or small-caps;}
    영어를 작은 대문자로 표시해주는 속성

+ **font-style** : 선택자{font-style: normal or italic or oblique;} 
    글자를 이텔릭체로 표시하는 속성

+ **font**

+ **color** : 선택자{color: 색상;} * 색지정방법 :  rgb(000, 000, 000) / red / #ff0000
    글자 색을 정하는 속성

### § 텍스트 스타일 

+ **text-decoration**
    글자 밑줄이나 취소선,윈 선을 긋는 속성

    |    |      |
    |---|----|
    |none|밑줄 삭제
    |underline|밑줄 표시
    |overline|윗줄 표시
    |line-through|취소선 표시

+ **text-transform**
    영문자를 표시할 때 대소문자를 원하는 대로 바꿀 수 있는 속성

    |    |      |
    |---|----|
    |none|변환 없이 표시
    |capitalize|시작하는 첫 번쨰 글자를 대문자로 변환
    |uppercase|모든 글자를 대문자로 변환
    |lowercase|모든 글자를 소문자로 변환

+ **text-shadow**
    텍스트에 그림자 효과를 주는 속성
    선택자{text-shadow: none or 가로 세로 번짐 색상;}
    * 인자(가로, 세로, 번짐, 색상)를 여러 개 사용할 때 “,“로 구분하여 그림자로 활용 가능
 
 + **white-space**
    공백을 처리하는 속성
    선택자{white-space: normal or nowrapor pre or pre-line or pre-wrap}
+ **letter-spacing**

+ **word-spacing**

### § 문단 스타일

+ **direction** 글자 쓰기 방향 지정
선택자{direction: ltr or rtl;}

+ **text-align** 문자 위치조정(정렬)
선택자{text-align: left or right or center or justify;}

+ **text-indent** 문장 들여쓰기
선택자{text-indent: 숫자(단위);}

+ **line-height** 문장끼리 줄간격 조정
선택자{line-height: normal or 숫자(단위);}

+ **text-overflow** 영역을 벗어나는 텍스트 표시 
선택자{text-overflow: clip or ellipsis;}

### § 목록 스타일

|   |   |    |
|---|---|----|
|ul|disc|흑색원형|
|  |circle|흰색원형|
|   |square|흑색사각형|
|   |none|기호표시안함|
|ol|decimal|1로 시작하는 십진수|
|  |decimal-leading-zero| |
|  |lower-roman/upper-roman| |
|  |lower-alpha/lower-latin|  |
|  |upper-alpha/upper-latin|  |

+ **list-style-image**
기호 대신 이미지 삽입
선택자{list-style-image: url(이미지 경로);}

+ **list-style-position**
목록 기호 들여쓰기
선택자{list-style-position: inside or outside;}

+ **list-style**
목록 스타일 한번에 지정하는 속성
선택자{list-style: type값 position값 image값;}


### 색상/배경

|구분|내용|표현 방법
|---|---|----
|영문 색이름|영문으로 색 이름 작성|red,black,blue 등
|16진수 표현| rgb값을 기준으로 16진수로 작성|#16진수 3자리 ex. #ff0000 (빨간색)
|rgb/rgba| rgb값을 0~255로 입력, rgba는 투명도 표현 가능 |rgb(0~255, 0~255, 0~255) ex. rgb(255, 0, 0) rgb(0~255, 0~255, 0~255, 0~1) 투명도 : 1 = 불투명 / 0=투명
|hsl/hsla| 색상,채도,밝기로 색 입력 | hsl(색상 값, 채도 값(%), 명도 값(%)) hsla(색상 값, 채도 값(%), 명도 값(%), 투명도)

### 배경 스타일

+ **background-color**
    배경색을 지정하는 속성
    선택자{background-color: 색상표현;}

+ **background-clip**
    배경 범위 조절
    선택자{background-clip: 속성 값;}

| | |
|-|-|
|border-box|박스 모델의 가장 외곽인 테두리까지 적용
|padding-box|테두리 제외한 패딩 범위까지 적용
|content-box|내용부문만 적용

+ **backgound-image**
배경에 이미지 설정
선택자{background-image: url(경로);}

+ **background-repeat**
배경 이미지 반복 출력 설정
선택자{background-repeat: 속성 값;}

+ **background-size**
배경 이미지 크기를 조절하는 속성
선택자{background-size: 속성 값;}

+ **background-position**
배경 이미지 위치를 조정하는 속성
선택자{background-position: 속성 값;}

+ **background-origin**
배경 이미지 배치할 때 기준을 지정하는 속성
선택자{background-origin: 속성 값;}

+ **background-attachment**
웹 페이지가 위아래로 움직여도 배경은 움직이지 않게 고정하는 속성
선택자{background-attachment: 속성 값;}

+ **background**
배경 이미지 한 번에 설정하는 속성
선택자{background: image값 repeat값 attachment값 position값 clip값 origin값 size값;}


### 포지셔닝
box모델, inline모델을 페이지 상에서 배치하는 스타일 즉, 페이지 안 요소들을 원하는 위치에 배치하는 속성 의미 position 속성, float 속성이 있음

+ **position**

    페이지의 요소를 자유롭게 배치해주는 속성 top, left, right, bottom으로 위치 지정
    선택자{position: 속성 값; [top: 숫자(단위);] [left: 숫자(단위);] [right: 숫자(단위);] [bottom: 숫자(단위);]}

+ **visibility**

    페이지에 특정 속성을 보이거나 보이지 않게 하는 속성
    선택자{visiblility: 속성 값;}

+ **z-index**

    페이지의 요소들을 순서대로 위에 쌓는 속성 속성 값이 크면 가장 위에 있는 요소, 작으면 밑에 있는 요소 * 요소가 항상 맨 위에 위치해야 하면 값을 999 또는 1000 등 큰 값으로 설정
    선택자{z-index: 속성 값;}

+ **float**
    페이지 내 요소의 위치를 왼쪽이나 오른쪽으로 지정하는 속성
    선택자{float: 속성 값;}

+ **clear**
    페이지에 float설정이 되어 있으면 그 속성이 그대로 그 다음 요소에 영향을 미치는데 이를 초기화시키는 속성
    선택자{clear: 속성 값;}

### 다단 스타일

+ **column-width**

    ```html
    단의 너비 고정하고 다단 구성 * 너비를 기준으로 다단 개수를 나눔
    선택자{
    -접두사-column-width: 숫자(단위) or auto; column-width: 숫자(단위) or auto;
    }
    ```
+ **column-count**

    ```html
    단의 개수를 지정하여 다단을 나눔
    선택자{
    -접두사-column-count: 숫자(단위) or auto; column-count: 숫자(단위) or auto;
    }
    ```
+ **column-gap**
    ```html
    다단 사이의 여백 설정
    선택자{
    -접두사-column-gap: 숫자(단위) or normal; column-gap: 숫자(단위) or normal;
    }
    ```

+ **column-rule**

+ **column-span**

### 표 스타일

+ **caption-side**
다단 사이의 여백 설정
선택자{
-접두사-column-gap: 숫자(단위) or normal; column-gap: 숫자(단위) or normal;
}
+ **width/height**
표 높이와 너비를 지정하는 속성으로 테이블에 지정하면 테이블의 전체 크기, <td>에 지정하면 컬럼의 너비/높이 표시
선택자{height: 숫자(단위); width: 숫자(단위);}

+ **border**
표의 테두리 스타일을 지정하는 속성 * 테두리 스타일 border속성 참고
선택자{border: width style color;}

+ **border-collapse**
테두리 스타일을 변경하는 속성으로 표 테두리를 두 개로 표시할 지 한 개로 표시할 지 결정
선택자{border-collapse: 속성 값;}

+ **border-spacing**
테두리를 두 개로 표현했을 때(separate) 가까운 쪽의 테두리 사이 거리 지정 속성
선택자{border-spacing: 가로 세로;}

+ **empty-celss**
테두리 스타일 두 개로 표시할 때(separate) 빈 셀에 대해 표시할 지 하지 않을 지 결정하는 속성
선택자{empty-cells: 속성 값;}

+ **table-layout**
```
<td>의 너비를 width로 지정해도 셀의 내용이 길어지면 자동으로 길어지고 table의 width 지정 값에 따라 안의 셀들이 조절되는데 <td>의 크기를 width로 고정하는 속성
선택자{table-layout: fixed or auto;} * 속성 값 auto는 default 값이며, fixed로 <td>를 고정한 상태에서 <td> 안의 내용이 넘어가면 <td>를 벗어나 작성이 됨 이를 <td> 안에 작성되게 하려면 word-break: break-all;을 추가하고 너비가 고정되면 작성 내용 길이에 따라 변경될 수 없으므로 자동으로 늘어날 수 있게 height 값을 auto로 정해 줌 height: auto;
```
+ **text-align**
<td>안의 텍스트를 수평으로 정렬하는 속성
선택자{text-align: left | center | right;}

+ **vertical-align**
<td>안의 텍스트를 수직으로 정렬하는 속성
선택자{vertical-align: top | bottom | middle;}


