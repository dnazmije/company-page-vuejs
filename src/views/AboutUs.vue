<template>
  <Navbar />
  <Heading heading='About Us' />
  <div>
    <p>
      Go to <router-link class='link' to='/products'>Products</router-link> page
      to see the list of products.
    </p>
  </div>
</template>

<script>
import Navbar from '@/components/Navbar.vue';
import Heading from '@/components/Heading.vue';

export default {
  name: 'AboutUs',
  components: {
    Navbar,
    Heading,
  },
};
</script>

<style scoped>
.link {
  color: #04778b;
  text-decoration: none;
}
</style>