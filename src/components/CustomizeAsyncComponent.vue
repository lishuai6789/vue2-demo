<template>
  <div>
    <p>Async</p>
    <el-table :row-key="getRowKey" border :data="arr">
      <el-column type="selection" :reserve-selection="true"></el-column>
      <el-column prop="aa">jfiwifwifw</el-column>
    </el-table>
    <el-button @click="handleClick">fwjfiwfiwfiw</el-button>
  </div>
</template>
<script>
export default {
  name: "CustomizeAsyncComponent",
  data() {
    return {
      arr: [
        {aa: 'a'},
        {aa: 'a'},
        {aa: 'a'},
        {aa: 'a'},
      ],
    };
  },
  methods: {
    getRowKey() {
      return "fwfw";
    },
    handleClick() {
      this.arr = [
        { aa: 'a' },
        { aa: 'a' },
        { aa: 'a' },
        { aa: 'a' },
      ];
    }
    
  }
};
</script>