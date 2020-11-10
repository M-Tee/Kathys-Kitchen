<template>
<footer>
  <div class="icons">
    <img src="../assets/icons/loactionMarker.svg" alt="Location Marker">
    <img src="../assets/icons/Insta.svg" alt="Instagram">
    <img src="../assets/icons/youtube.svg" alt="Youtube">
    <img src="../assets/icons/twitter.svg" alt="Twitter">
    <img src="../assets/icons/Email.svg" alt="Email Icon">
  </div>
  <p>
    ©2020 m-tee
  </p>
</footer>
</template>

<script>
export default {
  name: "footer"
}
</script>

<style scoped>
footer {
  background-color: #171717;
  color: #f1f6f7c2 !important;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  padding: 28px 0;
}

footer img {
  margin: 0 40px;
}

p {
  margin-top: 20px;
}
img {
  width: 25px;
}
</style>