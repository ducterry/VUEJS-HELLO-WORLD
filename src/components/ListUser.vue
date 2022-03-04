<template>
  <div class="list-user">
    <user v-for="user in listUser"
          v-bind:key="user.id"
          v-bind:user="user"></user>
  </div>
</template>

<script>
import User from "./User";

export default {
  name: "ListUser",
  props: {
    listUser: {
      type: Array,
      default: []
    }
  },
  data() {
    return {}
  },
  components: {
    User
  }
}
</script>

<style scoped>
.list-user {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
}

.list-user .user {
  padding: 20px;
  margin-bottom: 20px;
  border: 1px solid blueviolet;
  width: calc(33.33% - 20px);
}
</style>
