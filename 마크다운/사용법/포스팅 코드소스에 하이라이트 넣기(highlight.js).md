# 마크다운 이용 Tistory에 하이라이트 넣는법

> 기본적인 markdown.css만으로는 마크다운을 이용하여 포스팅 하는 경우
>
> codeblock에서의 하이라이트가 적용되지 않는다.
>
> 다른 방법도 있지만 여기서 Highlight.js를 이용한 방법을 소개하겠다.





## l. 공식 홈페이지에서 Highlight.js다운로드

### 1.공식 홈페이지 들어가기.

![image-20201015140125397](https://i.loli.net/2020/10/15/ln8OYP1CLca9UAJ.png)

[Highlight.js 공식홈페이지][]

홈페이지에서 Get version 버튼을 눌러서 들어가 준다.



### 2. 원하는 언어 선택하여 다운로드

![image-20201015140349166](https://i.loli.net/2020/10/15/7lxg3HNUiJEkwsu.png)



![image-20201015140440393](https://i.loli.net/2020/10/15/lwY1EKJxegH7a2R.png)





## ll. 티스토리 블로그 관리

1. 티스토리 블로그 관리 -> 꾸미기 -> 스킨편집

   <img src="https://i.loli.net/2020/10/15/omXMWaTfSi51QqK.png" alt="image-20201015140926584" style="margin-left:0px; zoom: 100%;"  />

   

2. 스킨 편집 -> html편집

   ![image-20201015142233196](https://i.loli.net/2020/10/15/LN6zJKZBYMrel1h.png)

   

3.  파일 업로드에서 추가버튼 클릭.

   ![image-20201015142429789](https://i.loli.net/2020/10/15/CkdwXJAiZE2m7sO.png)





## lll. highlight폴더 파일 추가 및 적용

![image-20201015143116829](https://i.loli.net/2020/10/15/F286J5keXtWOmpd.png)

처음에 받았던 highlight폴더에서 highlight.pack.js와 styles폴더에 있는 CSS파일로 자신이 입히고 싶은 테마를 업로드 할 수 있다.



![image-20201015144022513](https://i.loli.net/2020/10/15/3qGcjLSCrxpmIQJ.png)

[Highlight테마 데모보기][]

왼쪽 아래 Styles에 목록을 클릭하면 여러 가지 테마를 볼 수 있다. 필자는 GitHub테마를 좋아해서 GitHub테마로 적용.



### 파일 추가 위치 확인

![image-20201015150749029](https://i.loli.net/2020/10/15/dunKaPA4IGWZUkf.png)

추가 된 이후의 화면인데 여기서 추가된 파일의 위치는 **images** 디렉토리안에 들어가 있는걸 확인 할 수 있다.



### !중요

![image-20201015163228293](https://i.loli.net/2020/10/15/3lU6ycva4CPbMEk.png)

아까 간 html편집 화면으로 돌아간다.



![image-20201015163533764](https://i.loli.net/2020/10/15/C7QfjEmusiI9JcK.png)

해당 코드 삽입은 본인이 원하는 위치에 하면 되지만 자신이 추가한걸 보기 편하게 `</head>` 닫는 head태그 위에 추가해 주었다.(head태그는 아마 **40번째줄** 정도에 존재.) 여기서 **github.css** 파일은 자신이 원하는 테마의 CSS파일 이름으로 지정하면 된다. 필자는 github테마이므로... 



```html
<!-- 코드 하이라이트-->
<link href="./images/gihub.css" rel='stylesheet' type='text/css'>
<script src="./images/highlight.pack.js"></script>
<script>hljs.initHighlightingOnLoad();</script>
```

해당 코드는 위 코드를 복사해 가면 된다.



순서대로 따라하면 Typora로 마크다운을 작성하여 포스팅하게 되면 코드소스가 하이라이트 된 것을 확인할 수 있다.

Typora로 마크다운 작성하여 Tistory에 포스팅 하는 방법은 **마크다운 > 사용법**에서 확인하면 된다.





[Highlight.js 공식홈페이지]: https://highlightjs.org/
[Highlight테마 데모보기]:https://highlightjs.org/static/demo/