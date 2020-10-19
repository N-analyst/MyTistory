# Typora에서 글자 색 바꾸기

> Typora로 마크 다운을 이용해서 글을 작성하다 보면 글자 색을 바꾸고 싶을 때가 있다.
>
> Typora에서 글자 색을 바꾸려면 약간의 HTML, CSS의 지식이 필요하다.
>
> 크게 몰라도 밑에 내용을 따라하면 문제는 없다. 크게 어렵지 않다.





## HTML문법 사용하기

- Markdown 문법에서는 글자 색을 지정하는 문법이 존재하지 않는다.

- 여기서 해결책은 HTML태그를 사용하는 정도로 해결 가능하다.



### `<span></span>`

- `span`태그를 사용하여 바꾸고자 원하는 글자를 태그로 감싼다.
- `style`속성의 `color`를 이용하여 원하는 값으로 바꾼다.



```markdown
<span style="color:red">Red Text</span>
```



### !<span style="color:red">참고</span>

- 위 참고도 `span`태그를 이용하여 바꾼 것이다.
- 여기서 `color`의 값은 RGB값을 사용하여도 된다. ex) #b68834

