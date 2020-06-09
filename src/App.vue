<template>
  <div id="app">
    <el-container>
    <el-header>Header</el-header>
      <el-main>
        <el-row :gutter="20">
          <el-col :span="6"><div><hotwords></hotwords></div></el-col>
          <el-col :span="6"><div><bar></bar></div></el-col>
          <el-col :span="6"><div><hotwords></hotwords></div></el-col>
          <el-col :span="6"><div><bar></bar></div></el-col>
        </el-row>
      </el-main>
    </el-container>
  </div>
</template>

<script>
 import hotwords from './components/hotwords.vue'
 import bar from './components/bar.vue'

export default {
  name: 'App',
  components: {
    hotwords,
    bar
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 0px;
  width:100%;
  height:100vh;
  margin: 0 ;
  padding: 0 ;
  background-color:#000;

}
</style>
