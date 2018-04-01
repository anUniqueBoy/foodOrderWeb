<template>
  <div class="container">
    <div class="login-container">
      <h2 class="login-h2">个人中心</h2>
      <div class="login-form">
        <Form :model="formItem" ref="formItem" :rules="ruleItem" :label-width="80">
          <FormItem prop="phone" label="用户名：">
            <Input v-model="formItem.phone" size="large" placeholder="请输入手机号"></Input>
          </FormItem>
          <FormItem prop="password" label="密码：">
            <Input v-model="formItem.password" size="large" placeholder="请输入密码"></Input>
          </FormItem>
          <Button type="info" @click="handleSubmit('formItem')" long>登录</Button>
        </Form>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'PersonalCenter',
  data () {
    return {
      formItem: {
        phone: '',
        password: '',
      },
      ruleItem: {
        phone: [
          { required: true, message: '请输入手机号', trigger: 'blur' }
        ],
        password: [
          { required: true, message: '请输入密码', trigger: 'blur' },
          { type: 'string', min: 6, max:12, message: '密码长度不能小于或大于12', trigger: 'blur' }
        ]
      }
    }
  },
  methods: {

  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  /* 外层大背景图的样式 */
  .container{
    position: fixed;
    top: 0;
    right: 0;
    left: 0;
    bottom: 0;
    background: url(../assets/bg.jpg) no-repeat;
    background-size: 100% 105%;
    /* 设置背景颜色，背景图加载过程中会显示背景色 */
    background-color: #262626;
    display: flex;
    justify-content:flex-end;
    align-items: center;
  }
</style>
