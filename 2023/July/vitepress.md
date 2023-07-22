``` jsx
import { Fragment } from 'react'

import style from './Docs.module.scss'

const arr = [1, 2, 3, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1,1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1]


export default function Docs() {

return (

<Fragment>

<div className={style.wrapper}>

<header>

<ul>

<li><a href="">Guide</a></li>

<li><a href="">Refence</a></li>

<li><a href="">Beta-1</a></li>

<li><a href="">Github</a></li>

</ul>

</header>

<aside>

<div className={style.asideNav}>aside bg</div>

{arr.map(item => <div>{item}</div>)}

</aside>

<main>

<h1>main</h1>

</main>

<footer></footer>

</div>

</Fragment>

)

}

```

```scss
.wrapper {

display: flex;

flex-direction: column;

width: 100vw;

overflow: scroll;

  

header {

ul {

display: flex;

justify-content: space-between;

gap: 100px;

}

  

position: fixed;

top: 0;

width: 100vw;

height: 64px;

background-color: #1e1e20;

// z-index: 99;

border-bottom: 1px solid white;

}

  

aside {

margin-top: 64px;

padding-left: 100px;

position: fixed;

width: 272px;

box-sizing: border-box;

overflow: scroll;

height: 100%;

background-color: #161618;

color: white;

overscroll-behavior: contain;

// scrollbar-gutter: stable;

&::-webkit-scrollbar {

width: 10px;

}

  

&::-webkit-scrollbar-thumb {

background-color: #888;

border-radius: 5px;

}

}

  

main {

padding-top: 64px;

padding-left: 272px;

height: 2900px;

  

h1 {

color: white;

}

}

  
  

}
```