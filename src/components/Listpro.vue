<template>
<h1 class="title" v-if="rooms.id <= limited" >예능</h1>

<h1>예능</h1>
<Comedypro @openDoor="Modalopen = false; Clickdata = b" 
:rooms="rooms[b]" :limited="limited" v-for="(a,b) in rooms" :key="b"/>

<h1 >영화</h1>
<Comedypro @openDoor="Modalopen = false; Clickdata = b" 
:Moviedata="Moviedata[b]" :limited="limited" v-for="(a,b) in Moviedata" :key="b"/>

</template>
/*
1.json파일을 분리
2.Comedypro에 각각 데이터 프롭스로 넘겨줌
3.끝

*/
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
      Moviedata : Object,

    },
    
    

}
</script>

<style>

</style>