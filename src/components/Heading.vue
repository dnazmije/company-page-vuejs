<template>
    <h3>{{heading}}</h3>
</template>

<script>
export default {
  name: 'Heading',
  props: {
    heading: String
  }
}
</script>

<style scoped>
    h3 {
        padding: 16px;
        color: #04778b;
        background-color: #dcf3f5
    }
</style>