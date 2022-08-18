<template>
<Sidebar/>
  <Accueil/>
</template>

<script>
import Accueil from './components/Accueil.vue';
import Sidebar from './components/Sidebar.vue';

export default {
  name: 'App',
  components: {
    Accueil,
    Sidebar
}
}
</script>


