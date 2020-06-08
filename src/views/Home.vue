<template>
  <div class="app-warpper">
   <div class="siderbar-container"></div>
   <div class="main-container"></div>
  </div>
</template>

<script>
export default {
  name: 'Home',
  components: {
    
  }
}
</script>

<style lang="less" scoped>
.app-warpper{
  display: flex;
  .siderbar-container{
    width: 300px;
    height: 100vh;
    border-right:1px solid #eaeefb
  }
  .main-container{
    flex: 1;
  }
}
</style>
