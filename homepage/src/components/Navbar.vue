

<template>
            <!-- menu navigation -->
        <div class="nav" id="navb"> 
                           <div id="toggle">
                <i class="indicator"></i>
                     </div>
            <div class="logo">
                    ARTISTIC

                    <span class="burger back" id="burger" ></span>
            </div>

        </div>

</template>


<script>

import {defineComponent, ref,  nextTick} from 'vue'

export default defineComponent({
  name: 'HelloWorld',


setup() {

// sidebar
const DarkMode = ref(false)
const DarkButton = () => DarkMode.value = !DarkMode.value


nextTick(() => {
// script pour le bouton du mode sombre
const body = document.querySelectorAll('.back'); //je crée une constante nav , j'indique que cette constante va selectionner la balise nav (avec querySelector)
const toggle = document.getElementById("toggle");//je crée une constante toggle , j'indique que cette constante va selectionner l'id toggle (avec getElementById) 
const nav = document.getElementById("navb");//je crée une constante toggle , j'indique que cette constante va selectionner l'id toggle (avec getElementById) 
toggle.onclick = function(){  //j'indique que lorsque l'on clique sur l'id alors elle va démarrer une fonction 
  toggle.classList.toggle("active"); //elle va ajouter la classe active a mon id toggle
  nav.classList.toggle("active");
  body.forEach(slide => {   //je fais une fonction foreach pour qu'a chaques élément possédant la class back on ajoute la class active
    slide.classList.toggle("active");
  });

}

})

return {
  DarkMode,
  DarkButton
}

},


})
</script>

