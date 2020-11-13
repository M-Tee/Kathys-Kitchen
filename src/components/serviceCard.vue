<template>
   <div class="card margin">
      <img :src= "require('../assets/' + service.image)" alt="" />
      <div class="service">
        <h4 class="name"> {{service.name}} </h4>
        <div class="description"> {{service.description}} </div>
      </div>
    </div>
</template>

<script>
export default {
  name: "serviceCard",
  props: ["service"]
}
</script>

<style scoped>
.card {
  border-radius: 20px;
  display: flex;
  flex-direction: row;
  font-size: 1.4vw;
}
.container {
  align-content: space-around;
  padding-bottom: 30px;
}
img {
  border-radius: 20px;
  height: 40vh;
  margin-right: 20px;
  
}
.name{
  color: #d36200;
    font-size: 1.3em;
  font-weight: bold;
}
img,
.service {
  flex: 1;
}
.service {
  white-space: normal;
  margin: 30px;
  margin-top:  auto; 
  margin-bottom: auto;
}


</style>