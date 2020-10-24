<template>
  <div class="card">
    <img :src="require('@/assets/' + meal.image)" alt="image">
    <div class="details">
      <h3 id="name"> {{meal.name}} </h3>
      <p id="descrip"> {{ meal.description }} </p>
    </div>
  </div>
</template>

<script>

export default {
  name: "card",
  props: ["meal"]
}
</script>

<style scoped>
.card{
  flex-basis: 25%;
  background-color: #f1f6f7;
  margin: 0 20px 40px;
  /* padding: 20px; */
  box-shadow: 0px 8px 24px rgba(0, 0, 0, 0.15);
  border-radius: 20px;
  text-align: left;
}
.details{
  padding: 30px 20px;
}
#name{
  color: #d36200;
  margin-bottom: 7px;
  font-weight: normal;
  font-size: 1.8vw;
}
#descrip{
  font-weight: lighter;
  font-size: 1.4vw;

}
</style>
