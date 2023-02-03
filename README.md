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


