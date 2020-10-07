# startup-landing-page

Based on sections 8-9's content in [The Complete Web Developer in 2020: Zero to Mastery](https://www.udemy.com/share/101WcUAEIZc1ZVQXUH/) by @aneagoie. 

## RESOURCES
- original files by @aneagoie 
- google fonts: [fredoka one](https://fonts.google.com/specimen/Fredoka+One?query=Fredoka+One)
- bootstraps: [css](https://getbootstrap.com/docs/4.5/getting-started/introduction/)
- reading: [flex container](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Flexible_Box_Layout/Aligning_Items_in_a_Flex_Container), [vertical centering with css](https://vanseodesign.com/css/vertical-centering/#:~:text=centering%20in%20general.-,Vertical%2DAlign,to%20a%20value%20of%20auto.)
---
## STEP BY STEP
This section includes: download files, alter the head, divisions in the body and style, and button styling in css.
### 1. download files
  - index.html
  - style.css
  - header.jpg

### 2. alter the head
In the html file, 
  - copy the link of your font choice and insert after <title>
  ``` html
  <link href="https://fonts.googleapis.com/css2?family=Fredoka+One&display=swap" rel="stylesheet">
  ```
  - insert link of bootstrap css (the numbers before /css/bootstrap might be different, more updated version would have bigger numbers)
  ```html
  <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.5.2/css/bootstrap.min.css" integrity="sha384-JcKb8q3iqJ61gNV9KGb8thSsNjpSL0n8PARn9HuZOnIxN0hoP+VmmDGMN5t9UJ0Z" crossorigin="anonymous">
  ```
  - insert link of the stylesheet file, for example 
  ```html
  <link rel="stylesheet" type="text/css" href="style.css">
  ```

### 3. divisions in the body & style in css accordingly
To style specifically, give division to each part in html file and add class names if needed. I made three divisions in the body. They are accordingly used for "container", `<section>`, and "buffer". 
  ```html
  <body>
    <div class="container">
      <header>
        <h1>Hello, world!</h1>
      </header>
      <div>
        <section>
          <p>it's never too late to have the first startup</p>
          <div class="buffer"></div>
          <hr>
          <button type="button" class="btn btn-info">more</button>
        </section>
      </div>
    </div>
  </body>
  ```
  - in the body as `<div class="container"></div>`\
    In style.css file, call the container to style (display and grid-gap) and fit the screen width (grid-template-rows) as below. 
    ``` css    
    .container {
      display: grid;
      grid-gap: 20px;
      grid-template-rows: 1fr;
    }
    ```
  - for `<section>` after the `<header> as <div></div>`\
    This division is set for the section that contains with a paragraph, a buffer, a horizotal line, and a button. For styling in style.css file, I 
    ``` css
    p {
    color: #e2dbdb;
    text-transform: uppercase;
    font-family: 'Fredoka One', cursive;
    font-size: 14px;
    }

    .buffer{
      height: 4rem;
    }

    hr {
      border-color: #17a2b8;
      border-width: 3px;
      border-radius: 10px;
      max-width: 50px;
    }
    ```
  - in the `<section>` as `<div class="buffer"></div>`\
    Buffer is "a person or thing that prevents incompatible or antagonistic people or things from coming into contact with or harming each other (Definitions from Oxford Languages)". \
    This is, in my opinion, a styling matter which one would argue if it's better constructed within the css file. But I haven't encounter the method of doing so yet. 
    
### 4. button styling in css
 - with `.btn`, specify the text style (uppercased and font), set the border of the button (radius 500px and pad), and position it as relative.
``` css
.btn {
	text-transform: uppercase;
	font-family: 'Fredoka One', cursive;
	border-radius: 500px;
	padding: 1rem 2rem;	
	position: relative;
}
```
 - give `.btn-info` and `.btn-info:hover` information of original color and the change of color when mouse hops over the button
``` css
.btn-info {
    background-color: #17a2b8;
    border-color: #17a2b8;
}

.btn-info:hover {
    background-color: #28a3b9;
    border-color: #28a3b9;
    border-width: 3px;
}
```
 - (description to be continue)
``` css
.btn:not(:disabled):not(.disabled) {
    cursor: pointer;
}
```
---
## VALUABLE TAKEAWAYS (notes to myself)
- Styling with Bootstrap makes things so easy. Do more. 
- Vertical centering can be tricky. I need to work on this. 
- My new friend, `<html><body><div class="buffer"></div></body></html>`.
---
## DISCUSSIONS
Honestly, I am a thinker. I often think of questions that I don't know how to answer. Got any insight? Please, please, please do share with me. So, while doing this projects, I asked myself:  
1. Some suggests to style only in css to make sure that the html is clean with solely content matter data. But in ZTM, the majority of the styling @aneagoie shared is still happening in html. I wonder why this is the case. 
2. As a fresh meat in this field, I couldn't help but wonder if landing page is still a thing? Practically speaking, it is not much but a pretty face. It's a good practice for a rookie like me, but do users and employers really care about a pretty landing page? 
3. Just curious, how to make a "buffer" with css? 
