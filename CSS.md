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

