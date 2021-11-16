---
marp: true
theme: default
author: Nirand Pisutha-Arnond
paginate: true
footer: '255499: Web Application Development for IE'
---

<style>
    :root {
    font-family: kanit light;
}
div.colwrap {
  background-color: inherit;
  /* background-color: red; */
  color: inherit;
  width: 100%;
  height: 100%;
  position: relative;
}
/* div.colwrap div h1:first-child, div.colwrap div h2:first-child {
  margin-top: 0px !important;
} */
div.colwrap div.left {
  position: absolute;
  top: 0;
  bottom: 0;
  padding: 0px 0px 0px 0px;
}

div.colwrap div.right {
  position: absolute;
  top: 0;
  bottom: 0;
  padding: 0px 0px 0px 0px;
  /* display:flex;
  flex-direction: row;
  align-items: center; */
}


div.colwrap div.left {
/* background-color: green; */
  right: 50%;
  left: 0;
}
div.colwrap div.right {
  left: 50%;
  right: 0;
}
</style>

# Title

<div class="colwrap">
<div class="left">

- item
- `=IFS([@[Customer Age]]<25,"Youth",[@[Customer Age]]<35,"Young Adult", [@[Customer Age]] <65,"Adults",[@[Customer Age]]>=65,"Seniors") `
</div>
<div class="right inverted">

<iframe width="560" height="315" src="https://www.youtube.com/embed/Ppqnhj-gIss?start=726" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>
</div>

---

# Yes

- sdfs
-

```dax
=IFS([@[Customer Age]]<25,"Youth",[@[Customer Age]]<35,"Young Adult", [@[Customer Age]] <65,"Adults",[@[Customer Age]]>=65,"Seniors")
```

- sdfs
- dfsdf
- sdfs
- dfsdf

![bg contain right](./img/a.png)

---

```
=IFS([@[Customer Age]]<25,"Youth",[@[Customer Age]]<35,"Young Adult", [@[Customer Age]] <65,"Adults",[@[Customer Age]]>=65,"Seniors")
```
