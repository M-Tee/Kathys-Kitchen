<template>
  <div class="card">
    <img :src="content.image" alt="Image" />
    <div class="details">
      <p class="storyline">{{ content.phrase }}</p>
      <h3 class="name">{{ content.name }}</h3>
      <p class="description">
        {{ content.description }}
      </p>
    </div>
  </div>
</template>

<script>
export default {
  name: "s-card",
  props: ["content"],
};
</script>

<style scoped>
.card {
  margin: 0;
  display: flex;
  flex-direction: column;
  /* box-shadow: 0px 8px 24px rgba(0, 0, 0, 0.15);
  clip-path: inset(0px -15px 0px -15px);
  position: relative;
 */
}


img {
  width: 100%;
  height: 40vh;
}

.details {
  text-align: center;
  height: 31vh;
  padding: 1em;
  display: flex;
  flex-direction: column !important;
  justify-content: center;
  align-items: center;
}

.storyline {
  font-family: "Tillana", cursive;
  font-weight: 300;
  font-size: 0.8em;
}
.name {
  font-size: 1.3em;
  color: #d36200;
  font-weight: 600;
  margin: 20px 0;
}
.description {
  font-weight: lighter;
  white-space: normal;
}

@media only screen and (max-width: 768px) {
}

@media only screen and (max-width: 600px) {
  .card {
    box-shadow: 0px 8px 24px rgba(0, 0, 0, 0.15);
    border-radius: 20px;
  }
}
</style>