<template>
  <div class="navbar">
    <router-link
      v-for="route in menu"
      :key="route.url"
      :to="route.url"
      class="routerLink">
      {{ route.name }}
    </router-link>
  </div>
</template>

<script>
import data from "../data/data.json";

export default {
  name: "Navbar",
  data() {
    return {
      menu: data.menu,
    };
  },
};
</script>

<style scoped>
.routerLink {
  padding: 16px 8px;
  color: white;
  text-decoration: none;
  align-items: flex-start;
}
.routerLink:hover {
  background-color: #04778b;
}

.navbar {
  padding: 16px 8px;
  background-color: #048aa1;
  overflow: hidden;
  display: flex;
}
</style>
