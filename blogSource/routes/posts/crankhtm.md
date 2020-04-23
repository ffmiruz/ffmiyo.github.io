---
template: post.html
title: Use crank.js without JSX transpiling
date: 2020-04-23
---
If you'd like to avoid transpiling JSX, you can use HTM instead. HTM is less beautiful than JSX, but it's easier to set up.
```javascript
<script type="module">
  import {createElement} from "https://unpkg.com/@bikeshaving/crank?module";
  import {renderer} from "https://unpkg.com/@bikeshaving/crank/dom?module";
  import htm from 'https://unpkg.com/htm?module'
  const h = htm.bind(createElement);

  function Greeting({name = "World"}) {
    return h`
      <div>Hello ${name}</div>
    `;
  }
  renderer.render(h`<${Greeting} />`, document.body);
</script>
```