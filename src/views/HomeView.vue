<template>
  <div class="home">
    <h1>All Destinations</h1>
    <!-- <button @click="addDynamicRoute">Add Dynamic Route</button>
    <AppLink to="/dynamic">Visit Dynamic Route</AppLink> -->
    <div class="destinations">
      <router-link
        v-for="destination in destinations"
        :key="destination.id"
        :to="{
          name: 'destination.show',
          params: { id: destination.id, slug: destination.slug },
        }"
      >
        <h2>{{ destination.name }}</h2>
        <img :src="`/images/${destination.image}`" :alt="destination.name" />
      </router-link>
    </div>
  </div>
</template>

<script>
import sourceData from "@/data.json";
export default {
  data() {
    return {
      destinations: sourceData.destinations,
    };
  },
  methods: {
    addDynamicRoute() {
      this.$router.addRoute({
        name: "dynamic",
        path: "/dynamic",
        component: () => import("@/views/LoginView.vue"),
      });
    },
  },
};
</script>
