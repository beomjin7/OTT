<template>
  <swiper
    :cssMode="true"
    :navigation="true"
    :pagination="true"
    :mousewheel="true"
    :keyboard="true"
    :modules="modules"
    class="mySwiper"
  >
<swiper-slide>
  <h1 class="title">예능</h1>
  <Comedypro 
  :rooms="rooms[b]"  v-for="(a,b) in rooms" :key="b" />
</swiper-slide>
<swiper-slide>
  <h1 class="title">영화</h1>
  <Moviepro 
  :Moviedata="Moviedata[b]" s v-for="(a,b) in Moviedata" :key="b"/>
</swiper-slide>

</swiper>




    
</template>

<script>

import Comedypro from "./Comedypro.vue";
import Moviepro from "./Moviepro.vue";
import { Swiper, SwiperSlide } from "swiper/vue";

// Import Swiper styles
import "swiper/css";

import "swiper/css/navigation";
import "swiper/css/pagination";



// import required modules
import { Navigation, Pagination, Mousewheel, Keyboard } from "swiper";

export default {
    name : 'Listpro',

    components : {
        Comedypro : Comedypro,
        Moviepro : Moviepro,
        Swiper,
        SwiperSlide,

    },
    props : {
      rooms : Object,
      Moviedata : Object,
      },
      setup() {
    return {
      modules: [Navigation, Pagination, Mousewheel, Keyboard],
    };
  },
}
</script>

<style>

</style>