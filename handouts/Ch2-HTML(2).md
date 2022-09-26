---
marp: true
---

# Chapter 2. HTML

## Web Digital Marketing Programming

---

<!--
paginate: true
theme: default
size: 16:9
footer: 국민대학교 경영대학원 디지털마케팅 MBA,  Wooyoung Choi, 2022
-->

## Container, Symentic Elements

---

## Content division element - div

- 컨텐츠 블록을 구성하고 컨트롤 하기 위한 요소
- 만약 구성하고자 하는 블록이 섹션의 의미를 가지면 적절하지 않음

```html
<div class="container">
  <div class="box">
    <p>Ad section 1</p>
  </div>
</div>
```

---

## Content span element - span

- 인라인 컨텐츠를 그룹핑 하기 위한 요소
- 특정 부분에 스타일 지정이나 언어 명시를 위해 사용

```html
<section>
  <h1>Animals</h1>
  <ul>
    <li>토끼(<span lang="en">Rabbit</span>)</li>
    <li>코끼리(<span lang="en" style="font-size:20px;">Elephant</span>)</li>
  </ul>
</section>
```

---

## symantic tags

- 기존의 HTML의 문제: 요소가 의미를 지니지 않았음
- HTML5: main, nav, section, article, aside, header, footer 를 추가
- 구조적 의미를 지닐 수 있게 됨

---

## Dominant area element - main

- 문서의 가장 중요한(dominant) 부분을 표현하기 위한 요소
- 문서에서 유일해야 함

```html
<main>
  <article></article>
  <article></article>
  <article></article>
</main>
```

---

## Generic section element - section

- 컨텐츠의 장이나 절 등을 구분하기 위한 요소
- section 요소 안에는 제목요소를 사용하여 섹션의 제목을 명시해야 함

```html
<section>
  <h1>대한민국 헌법</h1>
  <section>
    <h2>제 1장 총강</h2>
    ...
  </section>
  <section>
    <h2>제 2장 국민의 권리와 의무</h2>
    ...
  </section>
</section>
```

---

## Article content element - article

- 문서에서 독립적으로 제공되거나 재사용되는 컨텐츠를 나열할 때 사용하는 요소
- Post, News article, Product Card, Comment, Widget 등

```html
<article class="posts">
  <article class="post">
    <h2>Post title</h2>
    <p>description..</p>
  </article>
  <article class="post">
    <h2>Post title</h2>
    <p>description..</p>
  </article>
</article>
```

---

## Navigation section element - nav

- 내비게이션 링크나 메뉴를 표현하기 위한 요소
- menus, tables of contents, index 등

```html
<nav class="main-nav">
  <ul>
    <li>Home</li>
    <li>Shop</li>
    <li>About</li>
  </ul>
</nav>
```

---

## Aside element - aside

- 메인 컨텐츠와 연관성이 떨어지는 컨텐츠를 표현하기 위한 요소
- Side bar, Ad section 등

```html
<aside>
  <h2>Recent posts</h2>
  <ul>
    <li>Post 1</li>
    <li>Post 2</li>
    <li>Post 3</li>
  </ul>
</aside>
```

---

## Introductory content element - header

- 페이지나 섹션 헤더를 표현하기 위한 요소

```html
<header>
  <img src="logo.png" alt="site-logo">
  <nav>..</nav>
</header>
<section>
  <header><!-- Section header--></header>
  ..
</section>
```

---

## Information content element - footer

- 페이지나 섹션 푸터를 표현하기 위한 요소

```html
<section>
  ..
  <footer><!-- Section footer--></footer>
</section>
<footer>
  <address>1, Cheongwadae-ro, Jongno-gu, Seoul, Republic of Korea</address>
  <p>Copyright &copy; KMU ALL RIGHTS RESERVED.</p>
</footer>
```

---

## Details disclosure element - details

- 사용자가 선택한 정보만 세부정보를 표현하고 싶을 때 사용하는 요소
- summary와 함께 사용
- open 속성으로 미리 열어둘 수 있음

```html
<details open>
  <summary>Abstract</summary>
  <span>Contents</span>
  <summary>Abstract</summary>
  <span>Contents</span>
</details>
```

---

## Data, User input tags

---

## Table content - table

- 2차원 형태의 데이터를 구조화할 때 사용하는 요소
- 문서 레이아웃을 위한 태그 사용은 접근성에 정확히 위반
  - [https://roy.gbiv.com/](https://roy.gbiv.com/)

- table > tr(row) > th(header), td(data) 의 자식구조

---

```html
<table>
  <caption>Mid-term exam result</caption>
  <thead>
    <tr>
      <th scope="col">No</th>
      <th scope="col">Name</th>
      <th scope="col">Grade</th>
    </tr>
  </thead>
  <!-- table body -->
</table>
```

---

```html
<!--table body -->
<tbody>
  <tr>
    <td>1</td>
    <td>John Doe</td>
    <td>80</td>
  </tr>
  <tr>
    <td>2</td>
    <td>Jane Doe</td>
    <td>70</td>
  </tr>
</tbody>
<!--table footer-->
```

---

```html
<!--table footer-->
<tfoot>
  <tr>
    <td colspan="2" scope="row">Average</td>
    <td>75</td>
  </tr>
</tfoot>
```

---

## Form element - form

- 유저 상호작용 폼 구성을 위한 요소
- 사용자가 입력한 정보를 미리 정의된 서버의 경로로 전달
- action: 정보를 제출할 경로
- method: 정보 제출 방법
  - GET: URL에 정보를 포함하여 전달(짧은 정보 제출에 유리)
  - POST: request body에 정보를 따로 전달(보안상 유리)

```html
<form action="/signup" method="POST">
  <!-- Form input -->
</form>
```

---

## Input element - input

- 유저로 부터 값을 전달받기 위한 상호작용 요소
- empty element
- type, id, name, required, minlength, maxlength, size 등의 속성을 지님

```html
<label for="user-id">Username: </label>
<input name="username" id="user-id" type="text" minlength="4" maxlength="20" size="22">
```

---

## [input types](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input)

- 모바일 등 사용성 향상을 위해 정확한 type 지정이 필요(UX, Accessibility)
- email, hidden, number, password, search, tel, text, url
- file, image
- checkbox, color, radio, range
- button, reset, submit
- date, datetime-local, month, time, week

---

```html
<input type="text" name="username" id="user-id" autofocus>
<input type="password" name="password" id="user-pw">
<input type="radio" name="" id="">
<input type="checkbox" name="" id="">
```

---

## HTML data list element - datalist

- option 태그와 함께 사용자가 입력할 값을 추천해주는 요소
- 다양한 input type에 적용 가능
  - text, search, url, tel, email, number
  - month, week, date, time, datetime-local
  - range, color

```html
<label for="user-movie">Choose your favorite movie</label>
<input list="movies" id="user-movie" name="movie">
<datalist id="movies">
  <option value="Dune"></option>
  <option value="Arrival"></option>
  <option value="Blade Runner 2049"></option>
</datalist>
```

---

```html
<input type="time" list="popularHours" />
<datalist id="popularHours">
  <option value="12:00"></option>
  <option value="13:00"></option>
  <option value="14:00"></option>
</datalist>
```

```html
<input type="range" list="tickmarks" />
<datalist id="tickmarks">
  <option value="0"></option>
  <option value="10"></option>
  <option value="20"></option>
  <option value="30"></option>
</datalist>
```

---

## Button element - button

- 버튼을 표현하기 위한 요소
- autofocus, disabled, type 등의 속성을 지님

```html
<button type="submit">가입</button>
<button type="reset">취소</button>
```

---

## HTML Select element - select

- 선택 옵션 패널을 표현하기 위한 요소
- required, disabled, autofocus 등 속성 지정

```html
<label for="coffee-menu">Choose a menu:</label>
<select name="coffee" id="coffee-menu">
  <option value="">--메뉴를 고르세요--</option>
  <option value="americano">아메리카노</option>
  <option value="latte">카페라떼</option>
  <option value="mocha">카페모카</option>
</select>
```

<link href="https://fonts.googleapis.com/css?family=Nanum+Gothic:400,800" rel="stylesheet">
<link rel='stylesheet' href='//cdn.jsdelivr.net/npm/hack-font@3.3.0/build/web/hack-subset.css'>

<style>
h1,h2,h3,h4,h5,h6,
p,li, dd, table > * > * {
font-family: 'Nanum Gothic', Gothic;
}
span, pre {
font-family: 'Hack', monospace;
}
</style>