<template>

<div class="mid" >
<img :src="movies.image" class="midimg" >
<p @click="post">{{movies.title}}</p>
</div>
</template>

<script>
export default {
    name: "Moivepro",
    methods : {
      post() {
        this.$emit('doorOpen', this.movies.id)
      }
    },
      props : {
      movies : Object,
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