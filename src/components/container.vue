<template>
<div class="container">
  <slot></slot>
</div>
</template>


<script>
export default {
  name: "container"
}
</script>

<style scoped>
.container{
  background-color: #f1f6f7;
  margin: 13px 7em;
  border-radius: 20px;
  display: flex;
  font-size: 1.4vw;
}

@media only screen and (max-width: 600px) {
 .container {
    flex-direction: column;
  }
 
}


</style>