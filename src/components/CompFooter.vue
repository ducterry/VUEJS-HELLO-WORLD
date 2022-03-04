<template>
  <h1>{{ titleFooter }}</h1>
</template>

<script>
export default {
  name: "CompFooter",
  props: {
    titleFooter: String
  },
  data() {
    return {
      textFooter: 'Hello Footer'
    }
  }
}
</script>

<style scoped>

</style>
