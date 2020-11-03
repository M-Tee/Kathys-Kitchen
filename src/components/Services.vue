<template>
  <div>
    <h2 class="heading">Service</h2>
    <div class="serviceCard">
    <serviceCard :key="service.id" v-for=" service in services" :service="service" />

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
          name: "service 1",
          description: "lorem ipsum",
        },
        {
           id: 2,
          name: "service 1",
          description: "lorem ipsum",
        },
         {
           id: 3,
          name: "service 1",
          description: "lorem ipsum",
        },
         {
           id: 4,
          name: "service 1",
          description: "lorem ipsum",
        },
      ],
    };
  },
};
</script>

<style scoped>
.serviceCard :nth-child(2),
.serviceCard :nth-child(4) {
  flex-direction: row-reverse;
}
</style>