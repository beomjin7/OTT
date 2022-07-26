<template>
<Navbar />
<transition name="fade">
<Modalopen @closeModal="Modalopen = ture" 
:Clickdata="Clickdata" :rooms="rooms" :Modalopen="Modalopen"/>
</transition>

<Listpro @openDoor="Modalopen = false; Clickdata = b" 
:rooms="rooms[b]" :limited="limited" v-for="(a,b) in rooms" :key="b" />


<hr>

<label for="file" class="input-plus" @click="addMovieData">+</label>



</template>

<script>
import Imgdata from './assets/Imgdata.js';
import Navbar from './components/Navbar.vue';
import Modalopen from './components/Modalopen.vue';

import Listpro from './components/Listpro.vue';







export default {
  name: 'App',  
  data() {
    return {
      rooms: Imgdata,
      Modalopen : true,
      Clickdata : 0,
      limited : 7,
    }
  },
  components : {
    Navbar: Navbar,
    Modalopen: Modalopen,
    Listpro : Listpro,
},
  methods : {
    addMovieData() {
      this.limited += 8;
    }
  }
}
</script>

<style>
body {
    background-color: #EAEAEA;
    text-align: center; 
}

.input-plus {
  cursor: pointer;
  font-size : 50px;
  
}

.fade-enter-from {
  transform: translateY(-1000px);
}
.fade-enter-active {
  transition: all 0.5s;
}
.fade-enter-to{
  transform: translateY(0px);
}

.fade-leave-from {
  transform: translateY(0px);
}
.fade-leave-active {
  transition: all 1s;
}
.fade-leave-to{
  transform: translateY(-1000px);
}

</style>