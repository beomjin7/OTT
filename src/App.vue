<template>
<Navbar />
<transition name="fade">
<Modalopen @closeModal="Modalopen = true" 
:Clickdata="Clickdata" :rooms="rooms" :Modalopen="Modalopen" :Moviedata="Moviedata" />
</transition>

<Listpro  
:rooms="rooms" :Moviedata="Moviedata" @openDoor="Modalopen = false"  />


<hr>


<label for="file" class="input-plus" v-if="movieOpen == true" >+</label>



</template>

<script>
import Cmddata from './assets/Cmddata.js';
import Moviedata from './assets/Moviedata.js';
import Navbar from './components/Navbar.vue';
import Modalopen from './components/Modalopen.vue';
import Listpro from './components/Listpro.vue';







export default {
  name: 'App',  
  data() {
    return {
      Moviedata : Moviedata,
      rooms : Cmddata,
      Modalopen : true,
      Clickdata : 0,
      movieOpen : true,
      
    }
  },
  components : {
    Navbar: Navbar,
    Modalopen: Modalopen,
    Listpro : Listpro,

  },
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
  border : none;
  background-color : #EAEAEA;

  
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