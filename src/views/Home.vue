<template>
  <div class="app-warpper">
    <div class="siderbar-container">
      <file-search v-model="searchTitle"></file-search>
      <file-list :fileList="fileList"></file-list>
    </div>
    <div class="main-container">
      <file-edit
        v-model="fileItem.content"
        :title.sync="fileItem.title"
        :boxShadow="false"
        :subfiled="false"
        :shortCut="false"
        @change="onSubmit"
      ></file-edit>
    </div>
  </div>
</template>

<script>
import FileSearch from "@/components/FileSearch";
import FileList from "@/components/FileList";
import FileEdit from "@/components/FileEdit";
export default {
  name: "Home",
  components: {
    FileSearch,
    FileList,
    FileEdit
  },
  data() {
    return {
      searchTitle: "",
      fileList: [
        { id: 1, title: "文件名 1", time: "2020-06-21" },
        { id: 2, title: "文件名 2", time: "2020-06-21" },
        { id: 3, title: "文件名 3", time: "2020-06-21" },
        { id: 4, title: "文件名 4", time: "2020-06-21" },
        { id: 5, title: "文件名 5", time: "2020-06-21" },
        { id: 6, title: "文件名 6", time: "2020-06-21" },
        { id: 1, title: "文件名 1", time: "2020-06-21" },
        { id: 2, title: "文件名 2", time: "2020-06-21" },
        { id: 3, title: "文件名 3", time: "2020-06-21" },
        { id: 4, title: "文件名 4", time: "2020-06-21" },
        { id: 5, title: "文件名 5", time: "2020-06-21" },
        { id: 6, title: "文件名 6", time: "2020-06-21" }
      ],
      fileItem:{
        title:'',
        content:''
      }
    };
  },
  methods: {
    onSubmit(value) {
      console.log(value)
      console.log(this.fileItem)
    }
  },
};
</script>

<style lang="less" scoped>
.app-warpper {
  overflow-x: hidden;
  display: flex;
  .siderbar-container {
    width: 300px;
    height: 100vh;
    border-right: 1px solid #eaeefb;
  }
  .main-container {
    flex: 1;
  }
}
</style>
