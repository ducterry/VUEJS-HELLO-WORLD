<template>
  <div class="comp-tabs">
    <div class="tab-title">
      <span>{{ title }}</span>
      <ion-icon name="alarm-outline"></ion-icon>
    </div>
    <div class="tab-content">
      <slot></slot>
    </div>
  </div>
</template>

<script>
export default {
  name: "CompTab",
  props: {
    title: String
  },
  data() {
    return {}
  }
}
</script>

<style scoped>
.tab-title{
  padding: 15px 30px;
  border: 2px solid #015;
  display: flex;
  justify-content: space-between;
}

.tab-header{
  margin: 0;
  padding: 0;
  list-style-type: none;
  display: flex;
}
.tab-header li{
  padding: 8px 15px;
  background-color: #999;
  transition:  all .3s;
}

.tab-header li:hover{
  background-color: #333;
  color: #fff;
}

.tab-content{
  margin-top: 2px;
  padding: 2px;
  border: 2px solid #567;
}
</style>
