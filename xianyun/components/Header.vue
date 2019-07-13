<template>
  <div class="header">
    <el-row type="flex" class="main" justify="space-between">
      <nuxt-link to="/">
        <h1>闲云旅游</h1>
      </nuxt-link>
      <el-row type="flex" class="nav">
        <nuxt-link to="/">首页</nuxt-link>
        <nuxt-link to="/post">旅游攻略</nuxt-link>
        <nuxt-link to="/hotel">酒店</nuxt-link>
        <nuxt-link to="/air">国内机票</nuxt-link>
      </el-row>
      <el-row>
        <el-dropdown v-if="true">
          <el-row type="flex" align="middle" class="el-dropdown-link">
            <nuxt-link to="#">
                <img src="../static/pic_sea.jpeg" alt="">
              用户名
            </nuxt-link>
            <i class="el-icon-caret-bottom el-icon--right"></i>
          </el-row>
          <el-dropdown-menu slot="dropdown">
            <el-dropdown-item>
              <nuxt-link to="#">个人中心</nuxt-link>
            </el-dropdown-item>
            <el-dropdown-item>
              <div>退出</div>
            </el-dropdown-item>
          </el-dropdown-menu>
        </el-dropdown>
        <nuxt-link to="/user/login"  class="account-link" v-else>登录 / 注册</nuxt-link>
      </el-row>
    </el-row>
  </div>
</template>
<script>
export default {};
</script>
<style lang="less" scoped>
h1 {
  width: 150px;
  height: 50px;
  font-size: 0;
  margin-top: 9px;
  background: url(../static/logo.jpg) no-repeat;
  background-size: 150px 40px;
}
.header {
  height: 60px;
  box-shadow: 0 2px 3px #ccc;
}
.main {
  width: 1000px;
  margin: 0 auto;
  line-height: 60px;
}
.nav {
  flex: 1;
  padding: 0 20px;
  a {
    display: block;
    padding: 0 20px;
    height: 60px;
    &:hover {
      border-bottom: 5px #409eff solid;
      color: #409eff;
    }
  }
  /deep/.nuxt-link-exact-active {
    background: #409eff;
    color: #fff;
    &:hover {
      color: #fff;
    }
  }
}
.el-dropdown-link{
           margin-left:20px;

           &:hover{
               img{
                    border-color: #409eff;
               }
            }

           a{
               display:block;
           }

            img{

                width:32px;
                height:32px;
                vertical-align: middle;
                border:2px #fff solid;
                border-radius:50px;
            }
        }

        .account-link{
            font-size: 14px;
            margin-left:10px;
            color:#666;

            &:hover{
                color:#409eff;
                text-decoration: underline;
            }
        }
</style>