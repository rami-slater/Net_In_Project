<template>
<div class="home">
<div >
<el-steps :active="active"  align-center finish-status="success" >
  <el-step title="步骤1" icon="el-icon-edit" description="资料填写"></el-step>
  <el-step title="步骤2" icon="el-icon-edit" description="任务确认"></el-step>
  <el-step title="步骤3" icon="el-icon-edit" description="开始任务"></el-step>
  <el-step title="步骤4" icon="el-icon-edit" description="任务结束"></el-step>
  <el-step title="步骤4" icon="el-icon-edit" description="任务结束"></el-step>
  <el-step title="步骤4" icon="el-icon-edit" description="任务结束"></el-step>
</el-steps>
</div>

<div>
<el-row class="tac" :gutter="20">
  <el-col :span="12">
    <el-menu
      default-active="2"
      class="el-menu-vertical-demo"
      @open="handleOpen"
      @close="handleClose">
      <el-submenu index="1">
        <template slot="title">
          <i class="el-icon-location"></i>
          <span>导航一</span>
        </template>
        <el-menu-item-group>
          <template slot="title">分组一</template>
          <el-menu-item index="1-1">选项1</el-menu-item>
          <el-menu-item index="1-2">选项2</el-menu-item>
        </el-menu-item-group>
        <el-menu-item-group title="分组2">
          <el-menu-item index="1-3">选项3</el-menu-item>
        </el-menu-item-group>
        <el-submenu index="1-4">
          <template slot="title">选项4</template>
          <el-menu-item index="1-4-1">选项1</el-menu-item>
        </el-submenu>
      </el-submenu>
      <el-menu-item index="2">
        <i class="el-icon-menu"></i>
        <span slot="title">导航二</span>
      </el-menu-item>
      <el-menu-item index="3" disabled>
        <i class="el-icon-document"></i>
        <span slot="title">导航三</span>
      </el-menu-item>
      <el-menu-item index="4">
        <i class="el-icon-setting"></i>
        <span slot="title">导航四</span>
      </el-menu-item>
    </el-menu>
  </el-col>
  </el-row>

</div>


  </div>
</template>

<script>
// @ is an alias to /src
// import HelloWorld from '@/components/HelloWorld.vue'

export default {
  // name: 'Home',
  data() {
      return {
        active: 2,
        isCollapse: true
      };
    },

    methods: {
      next() {
        if (this.active++ > 2) this.active = 0;
      },
      handleOpen(key, keyPath) {
        console.log(key, keyPath);
      },
      handleClose(key, keyPath) {
        console.log(key, keyPath);
      }
    },
  components: {
    // HelloWorld
  }
}
</script>

<style scoped>
  .el-header, .el-footer {
    background-color: #B3C0D1;
    color: #333;
    text-align: center;
    line-height: 60px;
  }
  .el-menu-vertical-demo:not(.el-menu--collapse) {
    width: 200px;
    min-height: 400px;
  }
  
</style>