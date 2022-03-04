<template>
  <div class="user">
    <h3>Email: {{ user.email }}</h3>
    <h4>Trang thai: {{ user.active ? "HOT DONG" : "BI KHOA" }}</h4>
  </div>
</template>

<script>
export default {
  name: "User",
  props: {
    user: {
      type: Object,
      default: null
    }
  },
  data() {
    return {}
  },
}
</script>

<style scoped>
h4{
  font-family: Arial;
  color: blue;
}
</style>
