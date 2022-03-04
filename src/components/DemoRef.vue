<template>
<div class="demo-ref">
  <h1>Demo Ref</h1>
  <button v-on:click="handleClickInputFile" class="avatar">Thay đổi Avatar</button>
  <input ref="fileInputAvatar" type="file" style="display: none">
</div>
</template>

<script>
export default {
  name: "DemoRef",
  data(){
    return {}
  },
  methods:{
    handleClickInputFile(even){
      this.$refs.fileInputAvatar.click();
    }
  }
}
</script>

<style scoped>
.demo-ref{
  margin-top: 10px;
  padding: 10px 30px;
  border: 1px solid blue;
}
.avatar{
  color: #fff;
  border: 2px solid #333;
  padding: 12px 15px;
  background-color: #333;
  transition: all .3s ease;
}

.avatar:hover{
  color: #333;
  background-color: #fff;
}
</style>
