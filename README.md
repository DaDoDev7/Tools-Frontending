# Tools-Frontending

Burger menu

//HTML

<div class="hamburger" id="hamburger-12">
          <span class="line"></span>
          <span class="line"></span>
          <span class="line"></span>
        </div>

//CSS


#hamburger-12.is-active .line:nth-child(1){
  opacity: 0;
  -webkit-transform: translateX(-100%);
  -ms-transform: translateX(-100%);
  -o-transform: translateX(-100%);
  transform: translateX(-100%);
}

#hamburger-12.is-active .line:nth-child(3){
  opacity: 0;
  -webkit-transform: translateX(100%);
  -ms-transform: translateX(100%);
  -o-transform: translateX(100%);
  transform: translateX(100%);

}

BURGER FRECCIA SINISTRA

#hamburger-3.is-active .line:nth-child(1),
#hamburger-3.is-active .line:nth-child(3){
  width: 40px;
}

#hamburger-3.is-active .line:nth-child(1){
  -webkit-transform: translateX(-10px) rotate(-45deg);
  -ms-transform: translateX(-10px) rotate(-45deg);
  -o-transform: translateX(-10px) rotate(-45deg);
  transform: translateX(-10px) rotate(-45deg);
}

#hamburger-3.is-active .line:nth-child(3){
  -webkit-transform: translateX(-10px) rotate(45deg);
  -ms-transform: translateX(-10px) rotate(45deg);
  -o-transform: translateX(-10px) rotate(45deg);
  transform: translateX(-10px) rotate(45deg);
}


//MENU A SCOMPARSA CON SCROLL

var halfWindow = window.innerHeight / 2;
var navigation = document.querySelector(".top-button");

window.addEventListener("scroll", function(){
  var scrolled = window.scrollY;
  if(scrolled >= halfWindow){
      navigation.classList.remove('hide');
  } else {
      navigation.classList.add('hide');
  }
  
})

//EVENTO CLICK MENU A COMPARSA

//js

const btn = document.getElementById("btn");
const menu = document.getElementById("menu");

btn.addEventListener("click", function() {
  if (menu.style.display === "none") {
    menu.style.display = "block";
  } else {
    menu.style.display = "none";
  }
});

//html da mostrare

<ul id="menu" style="display: none;">
  <li>Opcion 1</li>
  <li>Opcion 2</li>
  <li>Opcion 3</li>
</ul

//html bottone

<button id="btn">Mostrar menú</button>

// lista effetti corso


Testo sottolineatura dinamica all'hover

.testo_da_sottolineare{
  position: relative;
  a:after {
    content: '';
    position: absolute;
    width: 100%;
    transform: scaleX(0);
    height: 2px;
    bottom: -5px; //outline and text distance
    left: 0;
    background-color: crimson;
    transform-origin: bottom right;
    transition: transform 0.25s ease-out;
  }
  a:hover:after {
    transform: scaleX(1);
    transform-origin: bottom left;
  }
}

Primo menu hamburger 

.burger1{
  transition: .3s all ease-in-out;
  &:hover{
    transform: rotate(180deg);
    box-shadow: inset -3px 0 0 rgb(201, 133, 7), inset 0 -3px 0 rgb(201, 133, 7), inset 3px 0 0 rgb(201, 133, 7), inset 0 3px 0 rgb(201, 133, 7);
  }
  &:hover div:nth-of-type(1),&:hover div:nth-of-type(3){
    width: 30%;
  }
}

Secondo menu hamburger

.burger2{
  transition: all 0.5s ease-in-out;
  div{
    transition: all 0.3s ease-in-out;
  }
  &:hover{
    box-shadow: inset -3px 0 0 transparent, inset 0 -3px 0 transparent, inset 3px 0 0 transparent, inset 0 3px 0 transparent;
  }
  &:hover div:nth-of-type(2){
    display: none;
  }
  &:hover div:nth-of-type(1),&:hover div:nth-of-type(3){
    top: 50%;
  }
  &:hover div:nth-of-type(1){
    transform: translate(-50%,-50%) rotate(-45deg);
  }
  &:hover div:nth-of-type(3){
    transform: translate(-50%,-50%) rotate(45deg);
  }
}

/************************************************************/


