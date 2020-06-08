<template>
  <div class="content-edit">
    <el-input class="file-title" v-model="currentTitle" placeholder="请输入标题" />
    <mavon-editor v-bind="$attrs" @save="onSave" v-on="$listeners" placeholder="开始你的笔记吧~" class="markdown-wrapper" />
  </div>
</template>

<script>
export default {
  name: "FileEdit",
  props:{
    title:String
  },
  data() {
    return {
      currentTitle: this.title
    }
  },
  methods: {
    onSave() {
      console.log('save');
    }
  },
  watch: {
    currentTitle(newValue) {
      this.$emit('updata:title',newValue)
    }
  },
};
</script>

<style lang="less" scoped>
.content-edit {
  .file-title {
    padding-left: 5px;
    height: 56px;
    line-height: 56px;
    font-size: 18px;
    font-weight: 500;

    /deep/ .el-input__inner {
      height: inherit;
      line-height: inherit;
      font-weight: inherit;
      border: none;
    }
  }
  .markdown-wrapper {
    height: calc(100vh - 56px);
    &.fullscreen {
      height: 100vh;
    }
  }
}
</style>
