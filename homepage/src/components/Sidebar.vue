<style lang="scss">
 @import "@/assets/scss/style.scss"; 
</style>


<template>
 <aside class="sidebar" id="sidebar" >
        <nav class="navi">
            <div class="nav__menu">
                <div class="menu">
                    <ul class="nav__list">
                        <li class="nav__item">
                            <a :href="url" class="nav__link ">Accueil</a>
                        </li>
                        <li class="nav__item">
                            <a href="#about" class="nav__link">A propos</a>
                        </li>
                        <li class="nav__item">
                            <a href="#experiences" class="nav__link">Experiences</a>
                        </li>
                        <li class="nav__item">
                            <a href="#work" class="nav__link">Projets</a>
                        </li>
                    </ul>
                </div>
            </div>
            <div class="nav__close" id="nav-close" >
             <font-awesome-icon icon="fa-solid fa-xmark" />
              
                
            </div>
        </nav>
</aside>
</template>


<script>

import {defineComponent, ref,  nextTick} from 'vue'

export default defineComponent({
  name: 'HelloWorld',
  props: {
    msg: String
  },
  // fonction pour le liens href
    data() {
    return {
      url: 'https://github.com/'
    }
  },


setup() {

// sidebar
const sidebarVisible = ref(false)
const toggleButton = () => sidebarVisible.value = !sidebarVisible.value


nextTick(() => {
  const navMenu = document.getElementById('sidebar'),
      navToggle = document.getElementById('burger'),
      navClose = document.getElementById('nav-close')

console.log({navClose}, {navMenu}, {navToggle})

      if(navToggle) {
        navToggle.addEventListener("click", () => {
          navMenu.classList.add('show-sidebar')
        })
      }

      if(navClose) {
        navClose.addEventListener("click", () => {
          navMenu.classList.remove('show-sidebar')
        })
      }
})

return {
  sidebarVisible,
  toggleButton
}

},


})
</script>
