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
}
img {
  width: 100%;
  flex: 1;
}

.details {
  text-align: center;
  padding: 1em;
  /* padding: 6em 1em; */
  flex: 4;
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