HTML 정리  
============

HTML: Hyper Text Markup Language(마크업 언어)  
##### 기본 레이아웃
```
<!DOCTYPE html>
<html>
    <head> // 헤드 태그는 웹브라우저에 보이지 않음
        <title> Page title </title>
    </head>
<body>
      // 실질적으로 나타나는 부분
</body>
</html>
```
#### 1. HTML Basics  
- Heading Elements: \<h1\>~\<h6\>
  - 숫자 커질수록 크기 작아짐  
  - 클로징 태그 존재  

- Text Elements
  - \<p\>: paragraph, 클로징 태그 존재, block elements(줄바꿈 적용 X)
  - \<br\>: 줄바꿈 기능(개행문자), 클로징 태그 없음
  - <\hr\>: 수평선 긋기

- Text formating
  - \<b\>, \<strong\> : 볼드체(둘의 차이는 b: 의미강조 아니고 그냥 굵게, strong: 의미를 강조)
  - \<i\>, \<em\> : 이탤릭체  
  - \<code\> : 코드포맷  
  - \<sup\> : 지수승(위쪽으로 쓰기)  
  - \<sub\> : 아래쪽으로 쓰기  

- HTML Quotations
  - \<abbr\> : title 속성, 클로징 태그 있음
  ```
  <p>The<abbr title="World Health Organization">WHO</abbr></p>
  ```

  - \<bdo\> : dir 속성, 거꾸로 읽기, 클로징 태그 있음
  - \<q\> : 큰따옴표 넣고싶은 부분, 클로징 태그 있음

- Special characters
  - &nbsp : Non breaking space (=스페이스 바)  
  - &lt : <
  - &gt : >
  - &quot : \"
  - &amp : \&

- 주석처리
```
<!-- 이건 주석 처리 된다 -->
```

- List elements
  - \<ul\> : 순서없는 리스트
  - \<ol\> : 순서있는 리스트
  ```
  <ul>
    <li>사과</li>
    <li>딸기</li>
  </ul>
  ```

- Link elements
  - \<a\> : 누르면 링크로 연결(단어, 이미지, 문장 모두 가능), href 속성, target 속성
  ```
  <a href="http://www.google.com">Google</a>
  ```
  - target 속성
    - target="_blank" : 새탭 열기
    - target="_self" : 현재탭에서 열기

  - 한 페이지 내에서 부분 이동하기 : \<h1\>에서 id속성을 지정
  ```
  <a href="#id">___</a> // ____누르면 id의 헤드 부분으로 이동
  ```

- Image elements
  - \<img\> : 클로징 태그 없음, alt 속성은 이미지 안뜰 때 대안으로 텍스트 출력
  ```
  <img src="파일명" width="300" height="200" alt="CBNU">
  ```

- Table elements
  - \<table\> : 테이블 만들기, \<tr\>-가로줄 만들기, \<td\>-내용 채우기, \<th\>- 굵은 글씨
  - rowspan="2" : 2행 합치기
  - colspan="2" : 2열 합치기

  ```
  <table border="1"> // 테이블 테두리 두껍게 출력
  <tr> // 가로줄
    <th>Name</th>
    <td>Luna</td>
  </tr>  
  <tr>
      <th rowspan="2">Telephone:</th>
      <td>12343</td>
  </tr>
  <tr>
  </tr>
  </table>

  ```
