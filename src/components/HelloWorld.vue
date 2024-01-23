<template>
  <div class="center">
  <el-table :data="tableData" border style="width: 60%">
  <el-table-column prop="sid" label="id"></el-table-column>
  <el-table-column prop="name" label="姓名"></el-table-column>
  <el-table-column prop="age" label="年龄"></el-table-column>
  <el-table-column prop="birthday" label="生日"></el-table-column>
</el-table>

  </div>
</template>

<script>
import axios from 'axios';

  export default {
    name: 'HelloWorld',
    data() {
      return {
        tableData: [],
      };
    },
    created:function () {
      this.fetchDate();
    },
    methods: {
      fetchDate() {
        axios.get("http://localhost:8081/User").then((respond) => {
          this.tableData = respond.data
        }).catch((error) => {console.error('Error fetching data', error)})
      }
    },
    mounted:function () {
      console.log("app was mounted")
    },
    }
</script>

<style scoped>
  .center {
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
  }
</style>