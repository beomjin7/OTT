<template>
<h1 class="title" v-if="rooms.id <= limited" >예능</h1>

<Comedypro @openDoor="Modalopen = false; Clickdata = b" 
:rooms="rooms[b]" :limited="limited" v-for="(a,b) in rooms" :key="b" />

</template>

<script>

import Comedypro from "./Comedypro.vue";


export default {
    name : 'Listpro',
    data() {
      return {
        
      }
    },
    components : {
        Comedypro : Comedypro,

    },
    props : {
      rooms : Object,
      limited : Number,

    },
    
    

}
</script>

<style>

</style>