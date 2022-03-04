<template>
  <header>
    <h1>{{ titleHeader }} <br>
      <button v-on:click="changeTitleFromHeader">Thay đổi tile của App từ Component header</button>
    </h1>
  </header>
</template>

<script>
export default {
  name: "CompHeader",
  props: {
    titleHeader: String
  },
  data() {
    return {
      textHeader: 'Hello Footer'
    }
  },
  methods: {
    changeTitleFromHeader() {
      const data = {
        title: 'Title => Tu Component Header'
      };
      this.$emit('changeTitleEven', data);
    }
  }
}
</script>

<style scoped>

</style>
