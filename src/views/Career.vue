<template>
  <Navbar />
  <Heading heading='Career' />
</template>

<script>
import Navbar from '@/components/Navbar.vue';
import Heading from '@/components/Heading.vue';

export default {
  name: 'Career',
  components: {
    Navbar,
    Heading,
  },
};
</script>