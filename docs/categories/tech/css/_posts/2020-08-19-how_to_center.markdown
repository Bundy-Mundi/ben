---
layout: post
title:  "How to center your divs"
date:   2020-08-19 16:06:00 +0900
author: Ben Kweon
big_category: tech
sub_category: css
---

## Let's face it, it's really annoying and zero-fun.

It's always been challenging to center divs for develpers, not only in their beggining, but also after some experiences in dealing with css.

### *HTML

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <link rel="stylesheet" href="./style.css">
  <title>Document</title>
</head>
<body>
  <div class="parent">
    <div class="children">I'm a child component</div>
  </div>
</body>
</html>
```

We are going to use this simple index.html😙.

### 1. flex

Having components centered with using **``flex``** is the most common css-trick. Let's dive into it!

```css
.parent{
  display: flex;
  /* flex-direction is optional */
  justify-content: center;
  align-items: center;
}
.children{
  height: 200px;
  width: 200px;
}
```

But even though you followed my code, you may not see the centered children component inside of parent component.

That's because we didn't give height and width to our parent component.

So let's add them!

```css
.parent{
  display: flex;
  justify-content: center;
  align-items: center;
  
  /* Add height and width */
  height: 100vh;
  width: 100%;
}
.children{
  height: 200px;
  width: 200px;
  background-color: tomato;
}
```

Now you'd see perfectly centered children component😁.

### 2. transform

There is another way that you can accomplish this task with using **``position``** property.

This is the trick that I'd love to use whenever I need to deal with z-index with components, because this allows me to center components with using **``position: absolute;``** property.

```css
.parent{
  height: 100vh;
  width: 100%;
  position: relative;
}
.children{
   height: 200px;
   width: 200px;
   background-color: tomato;
   
   /* From here */
   position: absolute;
   top: 50%;
   left:50%;
}
```

But then you'd see that it's slightly off from center😥.

Let's add **``transform: translate(<X>, <Y>);``** property to do a little bit of trick!

```css
.children{
   height: 200px;
   width: 200px;
   background-color: tomato;
   
   /* From here */
   position: absolute;
   top: 50%;
   left:50%;
   transform: translate(-50%, -50%);
}
```
Now you can see centered div😁.

### 3. grid

Centering components with using **``grid``** property is quite new, but really strong. I'm pretty sure you all going to love it!


```css
.parent{
  height: 100vh;
  width: 100%;
  
  /* From here */
  display: grid;
  place-items: center;
}
.children{
   height: 200px;
   width: 200px;
   background-color: tomato;
}
```

It's so powerful and simple that we can just center items with only two lines of codes!

### Conclusion






