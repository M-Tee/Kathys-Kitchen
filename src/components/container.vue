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
  margin: 13px 100px;
  box-shadow: 0px 8px 24px rgba(0, 0, 0, 0.15);
  border-radius: 20px;
  display: flex;
  font-size: 1.4vw;
  line-height: 1.5;

}

</style>