<template>
    <Navbar />
    <Heading heading="Products"/>
    <ProductsTable />
</template>

<script>
import Navbar from '@/components/Navbar.vue';
import ProductsTable from '@/components/ProductsTable.vue';
import Heading from '@/components/Heading.vue'

export default {
  components: {
    Navbar,
    ProductsTable,
    Heading
  }
}
</script>