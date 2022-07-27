<template>
<div>
<h1 class="title" >예능</h1>
<Comedypro @openDoor="Modalopen = false; Clickdata = b" 
:rooms="rooms[b]"  v-for="(a,b) in rooms" :key="b"/>
</div>

<div v-if="openMenu == false">
<h1 class="title" >영화</h1>
<Moviepro @openDoor="Modalopen = false; Clickdata = b" 
:Moviedata="Moviedata[b]" s v-for="(a,b) in Moviedata" :key="b"/>
</div>

</template>

<script>

import Comedypro from "./Comedypro.vue";
import Moviepro from "./Moviepro.vue";


export default {
    name : 'Listpro',
    data() {
      return {
        
      }
    },
    components : {
        Comedypro : Comedypro,
        Moviepro : Moviepro,

    },
    props : {
      rooms : Object,
      limited : Number,
      Moviedata : Object,

    },
    
    

}
</script>

<style>

</style>