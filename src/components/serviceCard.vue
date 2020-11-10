<template>
   <div class="container margin">
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
.container {
  justify-content: space-between;
  align-content: space-around;
}
img {
  border-radius: 20px;
  height: 50vh;
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
  /* padding: 4em; */
  margin: 30px;
  margin: auto;
}


</style>