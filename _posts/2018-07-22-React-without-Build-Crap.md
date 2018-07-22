---
layout: post
title:  "React without Build Crap"
date:   2018-05-18 13:25:20 -0700
categories: jekyll update
---

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
</head>
<body>
    <div id="root"></div>
    <script crossorigin src="https://unpkg.com/react@16/umd/react.development.js"></script>
    <script crossorigin src="https://unpkg.com/react-dom@16/umd/react-dom.development.js"></script>
    <script type="text/javascript" src="test.js"></script>
</body>
</html>

```

```javascript
const e = React.createElement;

function NumberList(props) {
    const numbers = props.numbers;
    const listItems = numbers.map((number) =>
        e('li', null, number)
    );
    return (
        e('ul', null, listItems)
    );
}

const numbers = [1, 2, 3, 4, 5];

ReactDOM.render(
    e(NumberList, { numbers: numbers }, null),
    document.getElementById('root')
);
```