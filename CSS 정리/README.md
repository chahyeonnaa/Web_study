CSS 정리
============

#### 1. HTML과 CSS를 연결하는 3가지 방법
한 파일 내부에서 3가지 방법을 모두 써서 동시에 적용하면, 적용 우선순위는 (1. Inline, 2. External, 3. Internal)이다.
1. Inline : body태그 안에서 html 태그안에 css를 넣는 것
```
<!DOCTYPE html>
<html>
  <head>
  </head>
<body>
  <h1 style="color: red;">This is a heading1</h1>
  <p style="color: #0026ff;">This is a paragraph</p>
</body>
</html>
```

2. External : 외부 파일로 생성, head 태그 안에서 link 태그의 href 속성을 사용하여 연결
```
<!DOCTYPE html>
<html>
<head>
<link type="text/css" rel="stylesheet" href="mystyle.css">
</head>
<body>
<h1>This is a heading1</h1>
<p>This is a paragraph</p>
</body>
</html>
```

3. Internal : head태그 안에서 style태그 사용하여 적용
```
<!DOCTYPE html>
<html>
<head>
  <style>
  h1 { color: red; }
  p { color:#0026ff; }
</style>
</head>
<body>
</body>
</html>
```

#### 2. CSS Selectors(5가지)
1. Type Selector : 선택자 자리에 html요소 사용
```
<style>
h1 {
background-color: yellow;
border: 2px solid red;
}
</style>
```

2. ID Selector : html태그에서 선언된 id 속성 사용, '#' 사용, id는 파일 내에 유일해야함
```
<style>
#special {
background-color: yellow;
color: red;
}
</style>
```

3. Class Selector : html태그에서 선언된 class 속성 사용, '.' 사용, class명은 중복 허용
```
<style>
.type1 {
text-align: center;
}
</style>
```

4. Universal Selector : 모든 element에 적용, '*'사용  
```
<style>
*{
text-align: center;
color: red;
}
</style>
```

5. Css Grouping Selector  
• Simple combinatory (comma)  
• Descendant selector (space) : 자식을 포함한 후손들
• Child selector (>): 직속 자식들만
• Adjacent sibling selector (+): 첫번째 태그 바로 뒤에 나오는 형제만  
• General sibling selector (~): 첫번째 태그 뒤에 오는 모든 형제 선택

6. Attribute Selector
```
h1[title]{color:blue;}
p[class="example"]{color:blue;}
```

7. Pseudo-class Selector
```
selector:pseudo-class{
  property:value;
}
ex) a:link
    a:hover
    a:active
    a:visited
```
