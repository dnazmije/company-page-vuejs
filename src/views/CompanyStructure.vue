<template>
    <Navbar />
    <Heading heading="Company Structure" />
</template>

<script>
import Navbar from '@/components/Navbar.vue'
import Heading from '@/components/Heading.vue'

export default {
  name: 'CompanyStructure',
  components: {
    Navbar,
    Heading
  }
}
</script>