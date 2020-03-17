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




