<template>
<div class="mid" >
<img :src="Moviedata.image" class="midimg" >
<p @click="post">{{Moviedata.title}}</p>
</div>

<!--
<div>
<Moviepro @openDoor="Modalopen = false; Clickdata = b" />
</div>
-->
</template>

<script>



export default {
    name: "Moivepro",
    data(){
      return {
        
      }
    },
    methods : {
      post() {
        this.$emit('doorOpen', this.Moviedata.id)
      }
    },
      props : {
      Moviedata : Object,
      
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