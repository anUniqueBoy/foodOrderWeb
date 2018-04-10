<template>
  <div class="container">
    <div class="header">
      <div class="header-search">
        <Button type="info"  @click="jumpHome">返回首页</Button>
      </div>
      <div class="header-people" @click="jumpPeosonalCenter">
        <div style="width:30px;height:30px;">
          <img src="../assets/people.png" alt="" style="width:100%;height:100%;vertical-align:middle">
        </div>
        <p style="margin-left:5px">个人中心</p>
      </div>
    </div>
    <div class="content">
        <Row :gutter="24">
            <Col span="10">
                <div class="left-content">
                    <Carousel loop v-model="value">
                    <CarouselItem>
                        <div class="demo-carousel">
                            <img src="../assets/timg.jpg" style="width:100%;height:100%" alt="">
                        </div>
                    </CarouselItem>
                    <CarouselItem>
                        <div class="demo-carousel">
                            <img src="../assets/timg (1).jpg" style="width:100%;height:100%" alt="">
                        </div>
                    </CarouselItem>
                    <CarouselItem>
                        <div class="demo-carousel">
                            <img src="../assets/timg (2).jpg" style="width:100%;height:100%" alt="">
                        </div>
                    </CarouselItem>
                    <CarouselItem>
                        <div class="demo-carousel">
                            <img src="../assets/timg (3).jpg" style="width:100%;height:100%" alt="">
                        </div>
                    </CarouselItem>
                    </Carousel>
                </div>
            </Col>
            <Col span="14">
                <div class="right-content">
                    <ul class="right-top">
                        <li>
                            <span>价格：</span>
                            <b style="color:#e4393c">￥20</b>
                        </li>
                        <li>
                            <span>商品名称：</span>
                            <span>铁板培根饭</span>
                        </li>
                        <li>
                            <span>用户评分：</span>
                            <Rate allow-half v-model="valueHalf">
                                <span style="color: #f5a623">{{ valueHalf }}</span>
                            </Rate>
                        </li>
                    </ul>
                </div>
            </Col>
        </Row>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Detail',
  data () {
    return {
      value: 0,
      valueHalf: 4.8
    }
  },
  methods: {
    jumpPeosonalCenter() {
      this.$router.push({ name: 'PersonalCenter' });
    },
    jumpHome() {
      this.$router.push({ name: 'Home' });
    },
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  /* 外层大背景图的样式 */
  .container{
    position: absolute;
    top: 0;
    right: 0;
    left: 0;
  }
  .header{
    width: 100%;
    height: 60px;
    line-height: 60px;
    background-color: azure;
    /* background: url(../assets/bgheader3.png) no-repeat;
    background-size: 100% 100%; */
    display: flex;
    justify-content: space-between;
  }
  .header-search{
    margin-left:40px;
  }
  .header-people{
    margin-right:40px;
    display: flex;
    justify-content: center;
  }
  .header-people:hover{
    cursor: pointer;
  }
  .content{
    margin: 20px;
  }
  .right-content{
    text-align: left;
    font-size: 20px;
    height:28px;
    line-height: 35px;
  }
  .right-top li{
    list-style: none;
  }
</style>
