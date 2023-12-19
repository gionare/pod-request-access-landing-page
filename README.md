# Frontend Mentor - Pod request access landing page solution
## Table of contents
- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Continued development](#continued-development)
  - [Useful resources](#useful-resources)
- [Author](#author)
- [Acknowledgments](#acknowledgments)

## Overview

### The challenge

Users should be able to:

- View the optimal layout depending on their device's screen size
- See hover states for interactive elements
- Receive an error message when the form is submitted if:
  - The `Email address` field is empty should show "Oops! Please add your email"
  - The email is not formatted correctly should show "Oops! Please check your email"

### Screenshot

<img src="preview.jpg" alt="image preview" width= "400">

### Links

- Solution URL: [Github source code ](https://github.com/gionare/pod-request-access-landing-page)
- Live Site URL: [live site URL ](https://gionare.github.io/pod-request-access-landing-page/)

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- Mobile-first workflow
- Javascript
- [Styled Components](https://styled-components.com/) - For styles

### What I learned


```html
<form class="input_button">
          <input id="email" type="email" placeholder="Email address" required />
          <button class="btn" id="request-btn">Request access</button>
          <p id="error"></p>
        </form>
```

```css
.casts {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    position: relative;
    order: 2;
  }
  .casts img:nth-child(1) {
    width: 40px;
    height: 10%;
  }
  .casts img:nth-child(3) {
    width: 45px;
    height: 20%;
  }
```

```js
let input = document.getElementById("email");
let submit_btn = document.querySelector(".btn");
let error = document.querySelector("#error");
submit_btn.addEventListener("click", (event) => {
  event.preventDefault();
  const emailRegex = /^[a-zA-Z0-9._%+-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,}$/;
  if (emailRegex.test(input.value)) {
    error.innerText = "";
  } else {
    error.innerText = "Oops! Please check your email";
  }
});
```
### Continued development

continue focusing on in future projects. completely comfortable with useful techniques, want to refine and perfect.

## Author

- Website - [Giorgi Nareklishvili Portfolio](https://portfolio-giorgi-nareklishvili.vercel.app/)
- LinkedIn - [Giorgi Nareklishvili LinkedIn](https://www.linkedin.com/in/gionare/)

## Acknowledgments

@Bitcamp
@beqa200
