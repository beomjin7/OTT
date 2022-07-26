<template>
<div class="black-bg" v-if="Modalopen == false" >
  <div class="white-bg">
    <img class="room-img" :src="rooms[Clickdata].image">
    <h4>{{rooms[Clickdata].title}}</h4>
    <p>{{rooms[Clickdata].content}}</p>
    <button @click="$emit('closeModal')">닫기</button>
  </div>
</div>
</template>

<script>

export default {
    name : 'Modalopen',
    data() {
    return {
      
    }
  },
      components: { 
       
    },
    props : {
      rooms : Array,
      Modalopen : Boolean,
      Clickdata : Object,
    }



}
</script>

<style>
body {
  margin: 0;
}
div {
  box-sizing : border-box;
}
.black-bg {
    width: 100%;
    height: 100%;
    background: rgba(0,0,0,0.5);
    position: fixed;
    padding: 20px;
    display: flex;
    top: 0;
    left: 0;
    bottom: 0;
    justify-content: center;
    z-index: 100;
}
.white-bg {
    width: 50%;
    height: 100%;
    display: flex;
    background: white;
    border-radius: 8px;
    padding: 20px;
    flex-direction: column;
    align-items: center;
    justify-content: space-around;
}
.room-img {
  width:50%;
}

</style>