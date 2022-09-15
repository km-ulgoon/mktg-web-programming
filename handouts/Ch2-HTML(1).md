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

<div style="margin:auto;">
  <img src="./img/qr-repo.png" style="height:auto; width:400px;">
</div>

[https://github.com/km-ulgoon/mktg-web-programming](https://github.com/km-ulgoon/mktg-web-programming)

---

## HTML

- HyperText Markup Language
- 웹 컨텐츠의 구조와 의미를 정의하기 위해 사용

### Markup

- 텍스트, 이미지 등의 컨텐츠를 웹 브라우저에서 표현하기 위한 지시사항

---

## Web Standard

- 웹에서 표준적으로 사용되는 기술이나 규칙
- [W3C(the World Wide Web Consortium)](https://www.w3.org/standards/)의 토론을 통해 나온 권고안(recommendation)

### Non-standard

- marquee(IE)
- layer(Netscape)

---

### Importance of Web Standard

- 웹접근성 수준 향상
- 검색 친화적 웹사이트 구현
- 구조와 표현의 분리
- 유지보수 용이성, 비용절감
- 호환성

### 디지털 마케팅 관점에서 웹 표준의 중요성

- 유저에게 일관성있는 컨텐츠 제공
- 검색엔진 최적화

---

## Web Standard(HTML)

```html
<!doctype html>
<html lang="ko-KR">
<head>
  <meta charset="utf-8">
  <title>Title</title>
</head>
<body>
  <header>Page header</header>
  <nav>Navigation menu</nav>
  <main>
    <section>Content</section>
  </main>
  <aside>Sub content</aside>
  <footer>Page footer</footer>
</body>
</html>
```

---

## Web Accessibility

- 웹사이트에서 제공하는 정보를 차별 및 제한없이 동등하게 이용할 수 있도록 보장하는 것
- [W3C 웹 접근성 이니셔티브](https://www.w3.org/WAI/) 에서 지침 마련

## Pros

- 정보 소외 계층을 포함한 사용자층 확대
- 법적 요구사항 준수(장애인 차별 금지 및 권리 구제 등에 관한 법률)
- 다양한 환경,기기에서의 사용
- 개발 및 운영 효율성 제고

---

## [W3C 웹 접근성 이니셔티브](https://www.w3.org/WAI/)

- 인지성(Perceivable): 정보와 사용자 인터페이스 요소는 인지할 수 있도록 사용자에게 표시되어야 함
- 운용성(Operable): 사용자 인터페이스 요소와 탐색은 운용가능해야 함
- 이해성(Understandable): 정보와 사용자 인터페이스 운용은 이해할 수 있어야 함
- 견고성(Robust): 다양한 사용자 에이전트에 의존하여 해석될 수 있도록 내구성을 가져야 함

---

## 인지성

- 모든 텍스트가 아닌 콘텐츠에 대체 텍스트를 사람들이 원하는 인쇄, 점자, 음성, 기호 또는 간단 언어 등과 같은 형태로 제공해야 한다.
- 시간을 바탕으로 한 미디어에 대한 대안을 제공해야 한다.
- 정보와 구조의 손실 없이 콘텐츠를 다른 방식(예를 들면 더욱 간단한 형태로)들로 표현할 수 있어야 한다.
- 사용자들이 보다 쉽게 보고 들을 수 있는 전경에서 배경을 분리한 콘텐츠를 만들어야 한다.

---

## 운용성

- 키보드로 모든 기능을 사용할 수 있도록 해야 한다.
- 읽기 및 콘텐츠를 사용하는 사용자에게 충분한 시간을 제공해야 한다.
- 알려진 방법으로 발작을 일으킬 수 있는 콘텐츠를 디자인하지 않아야 한다.
- 사용자가 탐색하고, 콘텐츠를 찾고 그들이 어디에 위치하고 있는지를 알 수 있도록 도와주는 방법을 제공해야 한다.

---

## 이해성

- 텍스트 콘텐츠를 판독하고 이해할 수 있도록 만들어야 한다.
- 웹 페이지의 탑재와 운용을 예측 가능한 방법으로 제작해야 한다.
- 사용자의 실수를 방지하고 수정할 수 있도록 도와야 한다.

## 견고성

- 보조 기술을 포함한 현재 및 미래의 사용자 에이전트의 호환성을 극대화해야 한다.

---

## HTML

---

## Element

- HTML이 지시하기 위해 사용하는 기본 단위

- `<tagname attribute="value" empty-attribute>` 의 구조로 이루어짐 `</tagname>`
  - Empty elements: 내용이 없는 tag(img, link, meta, input, ..)
- `tagname`: 태그의 종류를 표현
- `attribute=""`: 태그의 속성을 정의
- `empty-attributte`: 값이 존재하지 않는 binary attribute

---

## Anatomy of an HTML document

```html
<!DOCTYPE html>
<html lang="ko-KR">
  <head>
	<!-- commentary -->
	<meta charset="utf-8">
	<title>First page</title>
  </head>
  <body>
	<!-- 
		multiline commentary
	-->
	<p>첫 페이지 내용</p>
  </body>
</html>
```

---

- `<!DOCTYPE html>` : 문서의 종류를 선언
- `<html></html>` : 한 페이지의 시작과 끝을 표현하기 위한 요소(root element)
- `<head></head>` : 페이지에 표현되지 않지만 필요한 정보를 정의하기 위한 요소
- `<body></body>` : 페이지에 표현될 정보를 정의하기 위한 요소
- `<!-- Commentary -->` : 주석 표현을 위한 요소(사용자에게 표현되지 않음)

---

## head elements

- `<meta>` : HTML의 메타정보 정의를 위한 요소
- `<title></title>` : HTML 문서의 제목을 표현하기 위한 요소
- `<link>` : 외부 리소스 연결을 위한 요소(이미지, 스타일시트 등)
- `<script></script>` : 실행가능한 코드 첨부를 위한 요소

---

### Metadata - `<meta>`

- `<meta charset="utf-8">` : 문서의 문자인코딩을 설정하기 위한 요소(웹 표준 인코딩: utf-8)
- `<meta name="title" content="My first page">`
- `<meta name="author" content="John Doe">`
- `<meta name="viewport" content="width=device-width, initial-scale=1.0">` : 화면영역 설정
- `<meta name="description" content="This site is to practice Web essentials">`
- `<meta property="og:image" content="img source url">`
- `<meta property="og:title" content="My first page">`
- `<meta property="og:description" content="This site is to practice Web essentials">`

---

[More info](https://developers.google.com/search/docs/advanced/crawling/special-tags)

[Open Graph Data](https://ogp.me/)

---

### External resouces - `<link>`

- `<link href="" rel="" type="">`

ex) `<link rel="stylesheet" href="public/style.css" type="text/css">`

---

### Style element - `<style>`

- `<style type="">`

ex)

```html
<style type="text/css">
  body {
  	background-color:#fff;
	line-height:1.4;
  }
</style>
```

---

### The Script element - `<script>`

- define and Execute script code
- `<script src=""></script>`
- default: 파일 다운로드가 끝날때 까지 HTML 파싱을 중단
- async: 파일 다운로드 완료시 바로 실행하며 HTML 파싱 중단
- refer: 파일 다운로드가 완료되어도 바로 실행하지 않고 HTML 파싱이 끝난 후 스크립트 실행

```html
<script>
  window.open("https://www.google.com/")
</script>
```

---

### alt content - `<noscript>`

- 웹 브라우저가 script 요소를 지원하지 않을 때 보여줄 대체 컨텐츠 지정

```html
<noscript>
  <a href="https://www.google.com" target="_blank">Go to google</a>
</noscript>
```

---

## Text, contents tags

---

## Heading text - h1~h6

- 제목 요소 표현을 위한 태그
- 컨텐츠의 제목을 표현 - SEO 관점에서 바람직한 제목 표현 방법
- 구조의 순서대로 h1~h6를 순차적으로 사용해야 함
  - h1 -> h2 -> h3(O)
  - h1 -> h3 -> h4(X)
- 컨텐츠의 의미 전달을 위해 사용
  - 섹션, 로고 등에 사용(이 경우, CSS 로 숨김처리)

---

## Paragraph text - p

- 텍스트 문단 표현을 위해 사용
- br 등의 인라인 요소 사용 가능
  - 시각적 효과를 위한 br 남발은 구조적으로 옳지 않음
  - ㅎ요할 경우 CSS로 처리

---

## List element - ol, ul, li

- 순서형(ol), 비순서형(ul) 목록 나열
- 메뉴 구성을 위해서 사용하기도 함
- ol 속성으로 reversed, start, type 지정 가능

```html
<ol>
  <li>Item 1</li>
  <li>Item 2</li>
</ol>
```

```html
<ul>
  <li>Item 1</li>
  <li>Item 2</li>
</ul>
```

---

## Anchor element - a

- 하이퍼링크 생성을 위한 태그
- href(hypertext reference), target(default=_self) 속성 지정

```html
<a href="https://www.google.com/">Go to google</a>
<a href="https://www.google.com/" target="_self">Go to google</a>
<a href="https://www.google.com/" target="_blank">Go to google</a>
```

---

## DRM-free Picture, Video Resources

- [https://www.pexels.com/](https://www.pexels.com/)
- [https://www.pexels.com/videos/](https://www.pexels.com/videos/)

---

## Image Embed element - img

- 이미지 참조를 위한 요소
- src: 이미지 경로 지정
- alt: 이미지가 보이지 않는 환경에서 제공할 대체 텍스트

```html
<img src="rabbit.png" alt="Rabbit is next to the bench.">
<img src="rabbit.png" width="300" height="200" alt="Rabbit is next to the bench.">
```

---

## Picture element - picture

- 0개 이상의 source 요소와 1개의 img 요소로 반응형 이미지 지원을 위한 요소
- picture 요소 미지원시 img 태그의 이미지를 지원

```html
<picture>
  <source srcset="elephant.png" media="(min-width: 720px)">
  <source srcset="cat.png" media="(min-width: 360px)">
  <img src="rabbit.png" alt="Rabbit is next to the bench.">
</picture>
```

---

## audio

```html
<audio controls="controls" preload="auto">
   <source src="media/tutorial.mp3" type="audio/mp3">
   <source src="media/tutorial.ogg" type="audio/ogg">
   <source src="media/tutorial.wav" type="audio/wav">
   <source src="media/tutorial.m4a" type="audio/mp4">
   <track label="Korean subtitles" kind="subtitles" srclang="ko" 
   src="tutorial_subtitles.vtt" default>
   <p>음성 파일 : <a href="media/tutorial.mp3">튜토리얼</a></p>
  </audio>
```

---

## video

```html
<video width="640" height="360" controls="controls" 
         poster="images/wave.jpg">
   <source src="media/wave.mp4" type="video/mp4">
   <source src="media/wave.webm" type="video/webm">
   <source src="media/wave.ogv" type="video/ogg">
   <track label="English subtitles" kind="subtitles" srclang="en" 
          src="wave_subtitles.vtt" default>
   <p>동영상 파일 : <a href="media/wave.mp4">파도 동영상</a></p>
  </video>
```

---

## Figure with optional caption element - figure

- 이미지, 비디오 등의 컨텐츠를 표현하기 위한 요소
- figcaption 으로 캡션 추가 가능(Optional)

```html
<figure>
  <img src="rabbit.png" alt="Rabbit is next to the bench.">
  <figcaption>Rabbit is next to the bench.</figcaption>>
</figure>
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