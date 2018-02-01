<template>
<div>
  <div id="head-nav" class="grid-content bg-purple-dark">
    <img src="../assets/logo.png" class="head-logo">
    <ul class="head-nav-list">
      <li @click="showLoginDialog = true">登录</li>
      <li class="nav-pile">|</li>
      <li >注册</li>
      <li class="nav-pile">|</li>
      <li >关于</li>
    </ul>
  </div>
  <el-dialog
    title="登录"
    :visible.sync="showLoginDialog"
    width="300px"
    :before-close="handleClose"
    >
    <div class="login-input">
      <el-input
        placeholder="请输入用户名"
        clearable
        prefix-icon="gil-icon-user-o"
        v-model="userName">
      </el-input>
    </div>
    <div class="login-input">
      <el-input
        placeholder="请输入密码"
        :type="showPassword ? 'text': 'password'"
        prefix-icon="gil-icon-lock-o"
        v-model="password">
        <i
          class="el-input__icon"
          :class="{'gil-icon-visible-o': showViewIcon && !showPassword, 'gil-icon-unseen-o': showViewIcon && showPassword}"
          slot="suffix"
          @click="handleIconClick">
        </i>
      </el-input>
    </div>
    <span slot="footer" class="diglog-footer">
      <el-button @click="showLoginDialog = false">取消</el-button>
      <el-button type="primary" @click="showLoginDialog = false">确认</el-button>
    </span>
  </el-dialog>
</div>
</template>

<script>
import '../assets/icon/iconfont.css'

export default {
  name: 'HeadNav',
  data() {
    return {
      showLoginDialog: false,
      showRegDialog: false,
      showAboutDialog: false,
      showPassword: false,
      userName: '',
      password: ''
    }
  },
  components: {
    
  },
  computed: {
    showViewIcon() {
      return this.password.length === 0 ? false : true
    }
  },
  methods: {
    handleClose(done) {
      this.$confirm('这是一条消息提示')
      .then(_=>{
        done()
      })
      .catch(_=>{})
    },
    handleIconClick(done) {
      this.showPassword = !this.showPassword
    }
  }
}
</script>

<style scoped>
  .bg-purple-dark {
    background: #498ee9;
  }
  .grid-content {
    z-index: 999;
    position: fixed;
    border-radius: 10px;
    width: 50%;
  }
  .head-logo {
    width: 50px;
    height: 50px;
    margin: 10px;
  }
  .head-nav-list {
    overflow: hidden;
    float: right;
    list-style: none;
    margin-right: 20px;
    margin-top: 25px;
  }
  .head-nav-list li {
    cursor: pointer;
    float: left;
    font-size: 16px;
    font: serif;
  }
  .nav-pile {
    padding: 0 10px;
  }
  .el-input {
    width: 95%;
  }
  .login-input {
    margin-top: 4%;
    margin-left: 0%;
    margin-right: 0%;
    text-align: center;
  }
</style>

