# In-class-exercise-2--Comp2112

### Change the book title (listed on right hand side)
```js
let title = document.querySelector('.item-page__main-title');
undefined
title
<h1 title=​"A Column Of Fire" data-a8n=​"item-page__main-title" class=​"item-page__main-title" style=​"word-wrap:​ break-word;​">​A Column Of Fire​</h1>​
title.textContent
"A Column Of Fire"
title.textContent = 'My favorite moment in my life'
"My favorite moment in my life"
title
<h1 title=​"A Column Of Fire" data-a8n=​"item-page__main-title" class=​"item-page__main-title" style=​"word-wrap:​ break-word;​">​My favorite moment in my life​</h1>​
title.textContent
"My favorite moment in my life"
```

### Change the book cover
```js
let photo = document.querySelector('.product-image__image--single');
undefined
photo.src
"https://dynamic.indigoimages.ca/books/052595497x.jpg?altimages=false&scaleup=true&maxheight=515&width=380&quality=85&sale=40&lang=en"
photo.src = "https://s-media-cache-ak0.pinimg.com/originals/d0/8f/d3/d08fd38e734d2cb6cd068141c56f4641.jpg";
"https://s-media-cache-ak0.pinimg.com/originals/d0/8f/d3/d08fd38e734d2cb6cd068141c56f4641.jpg"
photo
<img class=​"product-image__image--single" src=​"https:​/​/​s-media-cache-ak0.pinimg.com/​originals/​d0/​8f/​d3/​d08fd38e734d2cb6cd068141c56f4641.jpg" data-a8n=​"product-image__image" alt=​"A Column Of Fire by Ken Follett">

```

### Change the nav menus
```js
let optnav = ['Home','About Me','contact','Family','photo','video','Relation','hobbies','Passion'];
undefined
let Nmenu = Array.from(document.querySelectorAll('.top-nav__list-item'));
undefined
Nmenu.map( (Nav,index)=> Nav.textcontent = optnav[index]);
(10) ["Home", "About Me", "contact", "Family", "photo", "video", "Relation", "hobbies", "Passion", undefined]​

```
### Change logo by replacing the img element
```js
let main = document.querySelector('#headerImgLogo');
undefined
main
<img id=​"headerImgLogo" src=​"http:​/​/​www.georgiancollege.ca/​wp-content/​themes/​georgian/​imgs/​georgian-college-logo-colour-2017.svg" alt=​"Georgian College Accelerator Logo">​
let oldImg =document.querySelector('img');
undefined
let newimgs =document.createElement('img');
undefined
newimgs.src = "http://www.careersonthewater.ca/wp-content/uploads/2015/02/Georgian-720x340.jpg";
"http://www.careersonthewater.ca/wp-content/uploads/2015/02/Georgian-720x340.jpg"
newimgs
<img src=​"http:​/​/​www.careersonthewater.ca/​wp-content/​uploads/​2015/​02/​Georgian-720x340.jpg">​
newimgs.src
"http://www.careersonthewater.ca/wp-content/uploads/2015/02/Georgian-720x340.jpg"
main.replaceChild(newimgs, oldImg)
```
### Using a template literal with an object to change innerHTML
```js
const dietplain = {name:'michel burger',calories:'220',taste:'spicy'}
undefined
function render(dietplain){
    let snippet = `
     <h2>${dietplain.name}</h2>
     <ul>${dietplain.calories}</ul>
     <ul>${dietplain.taste}</ul>
`
    ;
    return snippet
}
undefined
let el = document.querySelector('.item-purchase__container');
undefined
el.innerHTML = render(dietplain)
"                                                                             
     <h2>michel burger</h2>
     <ul>220</ul>
     <ul>spicy</ul>
"
```
### Use a template literal within a template literal to create multiple ul-blocks
```js

const dietplain = [
    {'name':'michel burger','calories':'220','taste':'spicy'},
    {'name':'A & w burger','calories':'100','taste':'yummy'},
    {'name':'veggie burger','calories':'110','taste':'not bad'}];
undefined
function render(obj){
    let snippet =`
      ${dietplain.map ( dietplain => `
        <h2>${dietplain.name}</h2>
         <ul>
            <li>${dietplain.calories}</li>
            <li>${dietplain.taste}</li>
        </ul>
       `)};
   `;
    return(obj)
let el = document.querySelector('.item-purchase__container');
    el.innerhtml = render(dietplain)
}
undefined
let el = document.querySelector('.item-purchase__container');
undefined
el.innerHTML = render(dietplain)

```

### Make the book's author link go to www.georgiancollege.ca.

```js
let el = document.querySelector('.indigo-logo');
undefined
el.a = "http://www.georgiancollege.ca/"
"http://www.georgiancollege.ca/"

```

### Make the button to "Add to Cart" so that it erases the body.

```js
let el = document.querySelector('.common-button add-to-cart-button__primary ');
undefined
document.documentElement.innerHTML = el

```
