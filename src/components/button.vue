<template>
  <button class="btn">
    <slot></slot>
  </button>
</template>

<style scoped>
.btn{
  color: #ffffff;
  background-color: #D36200;
  border: none;
  border-radius: 50px;
  padding: 15px 30px;
}

</style>

<script>
export default {
  name: 'Button',
}
</script>