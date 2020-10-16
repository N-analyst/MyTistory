# 마크 다운 파일 포스팅 하는 방법

>Tistory에서 글을 작성할 때 마크 다운 파일의 내용을 그대로 포스팅 하기 유용.
>
>현재 포스팅 한 글도 Typora이용하여 쓴 글이다.



[github-markdown.css]:https://github.com/sindresorhus/github-markdown-css/blob/gh-pages/github-markdown.css

## 1. markdown.css 다운로드

### 1.1 CSS파일 받기

CSS파일을 받는 git 주소 <https://github.com/sindresorhus/github-markdown-css>

여기서 [github-markdown.css][] 파일을 받아 준다.

보기 편하게 **markdown.css**로 바꾸어 주었다.



### 1.2 CSS파일 변경

**markdown.css**파일 상단에 추가 할 내용.(CSS 파일을 열어서 아래 내용을 추가해 준다.)

```css
/* 추가 코드 시작부분 */
.markdown-body {
  box-sizing: border-box;
  min-width: 100px;
  max-width: 980px;
  margin: 0 auto;
  padding: 15px;
}

@media (max-width: 767px) {
  .markdown-body {
    padding: 15px;
  }
}
/* 추가 코드 끝 부분*/

/* 여기 부터는 원래 존재하는 코드*/
.markdown-body .octicon {
	...
}

```

위 코드는 해당 사이트에서 추가하라는 코드인데 html파일에 추가하라는 내용이지만,

우리는 계속 사용할 것 이므로 CSS파일에 추가해 준다.





## 2.  블로그 관리 홈

### 2.1 좌측 메뉴 꾸미기 > 스킨 편집 선택

<img src="https://i.loli.net/2020/10/16/QfVxXBKePjStwgv.png" alt="image-20201016133002603" style="margin-left:0px;" />



### 2.2 우측 상단 html편집 클릭

![image-20201016133151446](https://i.loli.net/2020/10/16/e7hOsaQFrm1jdK4.png)



### 2.3 파일 업로드> 추가 > markdown.css

<img src="https://i.loli.net/2020/10/16/x8oUZK9cSkYbslL.png" alt="image-20201016133440303" style="zoom:67%; margin-left:0px;" />

아까 받아서 이름을 **markdown.css**으로 바꾼 파일을 여기에 업로드한다.

이때 위치는 알아서 **images**폴더 안으로 들어간다.





### 2.4 HTML 탭 > `</head>`위 추가

<img src="https://i.loli.net/2020/10/16/cPtxuYNTW7UVz46.png" alt="image-20201016133904284" style="zoom:80%; margin-left:0px;" />

```html
<link rel="stylesheet" href="./images/markdown.css">
```

여기서 필자와 다른 이름으로 css파일을 만들었다면,

css파일 이름은 본인이 정한 이름으로 수정. 





## 3. Typora내보내기 + 포스팅에 적용

> 먼저 본인이 Typora로 작성한 내용이 있어야 함.



### 3.1 상단 메뉴 > 파일 > 내보내기 > HTML(without styles)

<img src="https://i.loli.net/2020/10/16/ihyqY7BrbWme2TR.png" alt="image-20201016140412218" style="zoom: 60%;" />



### 3.2 글쓰기

1. HTML선택.

   <img src="https://i.loli.net/2020/10/16/gwT1i25AakeXEIj.png" alt="image-20201016142744480" style="margin-left:0px;" />

   글쓰기에 들어가서 우측 상단의 dropbox에서 HTML선택. 





2. 아까 저장한 HTML파일을 열어서 우 클릭 > 페이지 소스 보기

   <img src="https://i.loli.net/2020/10/16/BpOq1IeWjdUcLT4.png" alt="image-20201016143436545" style="zoom:55%; margin-left:0px;" />

   클릭해서 나온 내용에서`<body></body>` 부분을 복사 한다.





3.  다시 포스팅 화면으로 돌아와서 내가 쓴 markdown 넣기

   <img src="https://i.loli.net/2020/10/16/UZcVFhD7xPjH4T3.png" alt="image-20201016144303391" style="margin-left:0px;" />

   사진과 같이 `<article class="markdown-body"></article>`사이에 `2`의 내용을 붙여 넣는다.

   

   ```html
   <article class='markdown-body'>
   	<!-- 2번에서 복사한 내용을 붙여 넣을 부분-->
   </article>
   ```



4. 마지막으로 카테고리와 제목을 입력하고 **완료**를 클릭한다.