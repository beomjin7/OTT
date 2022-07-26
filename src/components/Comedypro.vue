<template>

<div class="mid" >
<img :src="rooms.image" class="midimg" >
<p @click="send">{{rooms.title}}</p>
</div>
</template>

<script>
export default {
    name: "Comedypro",
    methods : {
      send() {
        this.$emit('openDoor', this.rooms.id)
      }
    },
      props : {
      rooms : Object,
      limited : Number,

    },
}
</script>

<style>
p {
    font-weight: bold;
    font-size: 20px;
}
.title {
  margin:0px 190px 15px;
  text-align: left;
}
.mid {
  display:inline-block;
  margin:5px 95px;
  
}
.midimg {
  width:100%;
  height:350px;
}


</style>