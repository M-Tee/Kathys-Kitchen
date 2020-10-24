<template>
 <div >
            <img :src="content.image" alt="Image">

            <div class="details">
              <p class="storyline" > {{content.phrase}} </p>
              <h3 class="name"> {{content.name}} </h3>
              <p class="description"> 
                  {{content.description}}
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

.details {
  padding: 100px 30px;
  text-align: center;
  flex: 2;
  font-size: 1.4vw;
}
img,
.details{
  /* flex: 1; */
}
.storyline {
  font-family: "Tillana", cursive;
  font-weight: 300;
}
.name {
  font-size: 2.0vw;
  color: #d36200;
  font-weight: 600;
  margin: 20px 0;
}
.description {
  font-weight: lighter;
 white-space: normal;
}
pre {
  font-family: Work Sans;
}

</style>