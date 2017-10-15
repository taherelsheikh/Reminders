# CSS
> - [Style](#style) 
> - [Style Tag](#style-tag)
> - [Link Tag](#link-tag)
> - Selector using class
> - Add two classes
> - !important
> - Two selectors
> - CSS VISUAL RULES


### style 

```html
  <p style="color: red; font-size: 20px; font-family: Arial;" >
Taher Elsheikh 
   </p>

```

### Style tag 

```html
<head>
  <style> p {font-family: Arial;} </style>
  <title>Vacation World</title>
</head>
```

### Link Tag
> Seperate the HTML and CSS code into two files and link them using the link tag

CSS in Style file 
> '#' is id and '.' is class

```html
p {font-family: Arial;}
h1 {color: maroon;}
#title-element {color: maroon;}
.title-element {color: red;}
```

HTML in index file

```html
<link href='./style.css' type='text/css' rel='stylesheet' >
```

### 4 - Selector using Class
CSS file

```html
.title{color: teal; text-transform: uppercase}
```

HTML file

```html
<p class="title">Sole Shoe Company</p>
```

### 5 - Add two classes

```html
<h1 class="title uppercase">Top Vacation Spots</h1>
```

### 6 - !important
> !important overrides any style no matter how specific they are. Not advised to use

CSS file

```html
h5 {
  color:rebeccapurple !important;
}
```

### 7 - Two Selectors - h5 and p 
CSS file

```html
h5, p {font-family: Georgia;}
```


### 8 - CSS VISUAL RULES
-  **font-size** controls the size of text displayed.
- **font-weight** defines how thin or thick text is displayed.
- The **text-align** property places text in the left, right, or center of its parent container.
- Text can have two different color attributes: **color** and **background-color**. color defines the color of the text, while background-color defines the color behind the text.
- CSS can make an element transparent with the **opacity** property.
- CSS can also set the background of an element to an image with the **background-image** property. 

#### Examples
- font-family: 'Playfair Display', serif;
- font-size: 14px;
- font-style: italic;
- background-color: white;
- color: black;
- opacity: 0.75;


