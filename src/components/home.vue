<template>
  <div class="container">
    <div class="header">
      <div class="header-search">
        <Input v-model="search" size="large" icon="ios-search-strong" width="300px" placeholder="Enter something..." style="width: 200px"></Input>
      </div>
      <div class="header-people">
        <Input v-model="value4" size="large" icon="ios-clock-outline" placeholder="Enter something..." style="width: 200px"></Input>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Home',
  data () {
    return {
      search: '',
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
  }
  .header{
    width: 100%;
    height: 80px;
    line-height: 60px;
    background: url(../assets/bgheader3.png) no-repeat;
    background-size: 100% 100%;
    display: flex;
    justify-content: space-between;
  }
  .header-search{
    margin-left:50px;
  }
</style>
