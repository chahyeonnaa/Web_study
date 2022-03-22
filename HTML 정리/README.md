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
#### 2. HTML Blocks
* Block elements : \<h1\>~\<h6\>, \<p\>, \<hr\>, \<ul\>, \<ol\>, \<li\>, \<table\>, \<div\>
  (항상 스크린 너비 전체를 차지하며, 새로운 라인부터 시작)  
  \<div\> : 컨테이너 생성(구역 나누기)  

  ```
  <div style="border: 3px solid red">
    <h2>Lion</h2>
    <p></p>
  </div>
  ```

* Inline elements : \<a\>, \<img\>, \<strong\>, \<i\>, \<em\>, \<sub\>, \<sup\>, \<span\>, \<label\> ,\<input\>
  (줄바꿈 안함)
  \<span\> : 텍스트에 컨테이너 생성

  ```
<body>
<p> This is an inline span <span style="border: 1px solid black">Hello</span>
</p>
  ```
#### 3. Multimedia elements
* Audio element, Video element
```
\<audio src="파일명" autoplay controls(다양한 속성들)><\audio>
\<vedio src="파일명" autoplay controls(다양한 속성들)><\vedio>
```    

* attributes
  - autoplay : 자동재생
  - controls : 재생/멈춤 버튼이 보임
  - loop : 반복재생
  - muted : 음소거 기능
  - src : 파일 위치
  - preload :
    auto - 비디오 전체가 사전 로딩, 버퍼링X  
    metadata - 사전로딩 X, 제일먼저 나오는 장면만 보여줌, 동영상 정보 제공(전체길이), 로딩한 것 처럼 보이지만 로딩은 아님  
    none - 사전로딩 X, 아무것도 안보임
  ```
  \<vedio src="파일명" preload="auto"><\vedio>
  ```

* Form element
```
<input type="button" value="Click here!"/> // 클로징 태그 없음
```  

  - 여러가지 input type
  ```
  <label> ID :</label> // 텍스트 박스 전에 뜨는 글자
  // text는 사용자에게 텍스트 입력 기능 제공
  <input type="text"><br> // inline element이므로 한 줄을 다 안잡아서 <br>태그 붙여야함
  ```
  ```
  // password는 사용자가 입력하는 글자가 dot으로 표기
  <input type="password"><br>
  ```
  ```
  // submit은 제출 버튼 제공 -> value값 지정해주지 않으면, 디폴트 텍스트로 Submit이 적힘
  <input type="submit" value="Login"><br>
  ```
  ```
  // reset버튼 제공 -> 입력된 모든 내용 초기화
  <input type="reset"><br>
  ```
  ```
  // radio 버튼 - 중복선택을 허용하지 않으려면, name속성에 같은 아이디값을 부여해야함
  <input type="radio" name="age">
  <label>항목1</label><br>
  <input type="radio" name="age">
  <label>항목2</label><br>
  ```
  ```
  // check 버튼 - 중복선택을 허용
  <input type="checkbox">
  <label>항목1</label><br>
  <input type="checkbox" checked> // 항상 체크되어있음
  <label>항목2</label><br>
  ```
 - input element 속성
 * autofocus : 페이지 로드 시, 커서가 자동으로 맞춰(깜빡깜빡)
 * placeholder : 연한 글씨로 뜨는거 (몇자만 입력하세요.) 같은거..
 * readonly : 입력할 수 없도록 잠금
 * required : 필수로 입력해야하는 부분, 작성안하면 다음페이지로 이동 불가
