<template>
  <div class="app-warpper">
   <div class="siderbar-container">
     <file-search ></file-search>
   </div>
   <div class="main-container"></div>
  </div>
</template>

<script>
import FileSearch from '@/components/FileSearch';
export default {
  name: 'Home',
  components: {
    FileSearch
  },
  data() {
    return {
       searchTitle: '',
    }
  },
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
