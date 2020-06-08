<template>
  <div class="search-container">
    <el-input placeholder="请输入内容" v-bind="$attrs" v-on="$listeners">
      <el-button slot="append" icon="el-icon-search"></el-button>
    </el-input>
    <el-dropdown trigger="click">
      <el-button type="primary" icon="el-icon-circle-plus-outline" circle></el-button>
      <el-dropdown-menu slot="dropdown">
        <el-dropdown-item @click="createFile">
          新建笔记
        </el-dropdown-item>
        <el-dropdown-item @click="importFile" divided>导入文件</el-dropdown-item>
      </el-dropdown-menu>
    </el-dropdown>
  </div>
</template>

<script>
export default {
  name: "FileSearch",
  methods: {
    createFile() {
      this.$emit('create')
    },
    importFile(){
      this.$emit('import')
    }
  },
};
</script>

<style lang="less" scoped>
.search-container{
  display: flex;
  align-items: center;
  padding: 12px 10px ;
  background:#daecfe;
  .el-dropdown{
    .el-button{
      margin-left: 10px;
      padding: 6px;
      font-size: 14px;
      border-radius: 30%;
    }
  }
}
</style>
