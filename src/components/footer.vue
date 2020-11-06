<template>
<footer>
  <div id="location">
    <img src="../assets/icons/loactionMarker.svg" alt="Location Marker">
    <p class="">New York</p>
  </div>
  <div id="socials">
    <img src="../assets/icons/Insta.svg" alt="Instagram">
    <img src="../assets/icons/youtube.svg" alt="Youtube">
    <img src="../assets/icons/twitter.svg" alt="Twitter">
  </div>
  <div id="email">
    <img src="../assets/icons/Email.svg" alt="Email Icon">
    <p>kathyneil@gmail.com</p>
  </div>
</footer>
</template>

<script>
export default {
  name: "footer"
}
</script>

<style scoped>
footer {
  background-color: rgba(0, 0, 0, 0.7);
  color: rgba(241, 246, 247, 0.76) !important;
  display: flex;
  flex-wrap: wrap;
  justify-content: space-around;
  padding: 30px 0;
  
}
#location,
#email{
display: inline-flex;
align-items: baseline;
}
p {
  margin-left: 10px;
}
#socials img{
  margin: 0 20px;
}
#socials,
#email {
  align-self:flex-end
}
img {
  width: 25px;
}
</style>