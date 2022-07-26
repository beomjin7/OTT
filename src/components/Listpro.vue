<template>
<h1 class="title" v-if="rooms.id <= limited" >예능</h1>

<Comedypro />

</template>

<script>

import Comedypro from "./Comedypro.vue";


export default {
    name : 'Listpro',
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