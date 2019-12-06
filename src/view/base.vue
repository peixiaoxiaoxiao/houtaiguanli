<template>
  <div class="base">
    <el-container>
      <el-header>Header</el-header>
      <el-container class="content">
        <el-aside width="200px">Aside</el-aside>
        <el-main>Main</el-main>
      </el-container>
    </el-container>
  </div>
</template>
<style lang="">
*{
    padding: 0;
    margin: 0;
}
.base{
    background: #ebebec;
}
.content{
    margin-top: 20px;
}
.el-header{
    display: flex;
    justify-content: space-around;
    background: #f7f7f7;
    align-items: center;
}
.el-aside{
    margin-left: 10px;
    margin-right: 10px;
    height: 100vh;
    background: #f7f7f7;
    overflow: auto;
}
.el-main{
    height: 100vh;
    background: #f7f7f7;
    overflow: auto;
    margin-right: 10px;
}
</style>