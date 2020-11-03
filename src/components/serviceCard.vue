<template>
   <div class="container margin">
      <img src="../assets/KathyS.jpg" alt="" />
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
img {
  border-radius: 20px;
  width: 10%;
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
  padding: 4em;
  margin: auto;
}


</style>