<template>
  <div id="">
    <h2 class="heading">Service</h2>
    <div class="serviceCard">
    <serviceCard id="card" :key="service.id" v-for=" service in services" :service="service" />
    </div>
  </div>
</template>

<script>
import serviceCard from "./serviceCard";
export default {
  name: "Services",
  components: {
    serviceCard,
  },
  data() {
    return {
      services: [
        {
          id: 1,
          image: "private.jpg",
          name: "Private Parties",
          description: "Planning a good time with friends and family, we got you covered. You make the memories I make the food. Let me."
        },
        {
          id: 2,
          image: "public.jpg",
          name: "Public Events ",
          description: "Large events can be hectic! You probably want to get the food right. Let me get that food impression right for you",
        },
         {
           id: 3,
          image: "amy-hirschi-uwpo02K55zw-unsplash.jpg",
          name: "Consulting",
          description: "Are you looking to venture into the food business? You could use a tip or two get you rolling. Lets get you started, talk to me!",
        },
         {
           id: 4,
          image: "cooking.jpg",
          name: "Cooking Lessons",
          description: "Its time to get wild with the ingredients in your kitchen. Meet your new cooking instructor, Kathy! Book that class.",
        },
      ],
    };
  },
};
</script>

<style scoped>
.serviceCard :nth-child(1),
.serviceCard :nth-child(3){
  /* padding-right: 50px; */
}

.serviceCard :nth-child(2),
.serviceCard :nth-child(4){
  flex-direction: row-reverse;
}


</style>