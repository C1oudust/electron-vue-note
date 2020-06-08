<template>
  <el-scrollbar class="file-list" wrap-class="scrollbar-filelist" :noresize="false" tag="ul">
    <li v-for="(item, index) in fileList" :key="index" class="file-item">
      <font-awesome-icon :icon="['fab', 'markdown']" class="item-icon" />
      <p class="item-title">{{ item.title }}</p>
      <p class="item-time">{{ item.time }}</p>
    </li>
  </el-scrollbar>
</template>

<script>
export default {
  name: "FileList",
  props: {
    fileList: {
      type: Array,
      default: () => []
    }
  },
  data() {
    return {};
  }
};
</script>

<style lang="less" scoped>
.scrollbar-filelist {
  height: calc(100vh - 56px);
  overflow-x: hidden !important;
}
.el-scrollbar__bar {
  opacity: 1;

  &.is-vertical {
    right: 0px;
    width: 5px;
    .el-scrollbar__thumb {
      background-color: rgba(144, 147, 153, 0.5);
    }
  }
}
</style>
