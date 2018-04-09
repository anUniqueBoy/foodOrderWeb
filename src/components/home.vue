<template>
  <div class="container">
    <div class="header">
      <div class="header-search">
        <Input v-model="search" icon="ios-search-strong" placeholder="Enter something..." style="width: 400px;"></Input>
        <Button type="info">搜 索</Button>
      </div>
      <div class="header-people" @click="jumpPeosonalCenter">
        <div style="width:30px;height:30px;">
          <img src="../assets/people.png" alt="" style="width:100%;height:100%;vertical-align:middle">
        </div>
        <p style="margin-left:5px">个人中心</p>
      </div>
    </div>
    <div class="content">
      <Row>
        <Col span="4">
          <ul class="left-content">
            <li>全部</li>
            <li>川菜</li>
            <li>火锅</li>
            <li>自助餐</li>
            <li>小吃快餐</li>
            <li>日韩料理</li>
          </ul>
        </Col>
        <Col span="20">
          <div class="header-content">
            <Carousel autoplay v-model="value" loop :autoplay-speed="3000">
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
      </Row>
    </div>
    <div class="show-container">
      <Row :gutter="16">
        <Col span="6">
          <div>
            <div>
              <img class="img-size" src="../assets/timg.jpg" alt="">
            </div>
            <p>千家粗粮王</p>
          </div>
        </Col>
        <Col span="6">
          <div>
            <div>
              <img class="img-size" src="../assets/timg.jpg" alt="">
            </div>
            <p>千家粗粮王</p>
          </div>
        </Col>
        <Col span="6">
          <div>
            <div>
              <img class="img-size" src="../assets/timg.jpg" alt="">
            </div>
            <p>千家粗粮王</p>
          </div>
        </Col>
        <Col span="6">
          <div>
            <div>
              <img class="img-size" src="../assets/timg.jpg" alt="">
            </div>
            <p>千家粗粮王</p>
          </div>
        </Col>
      </Row>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Home',
  data () {
    return {
      search: '',
      value: 0
    }
  },
  methods: {
    jumpPeosonalCenter() {
      this.$router.push({ name: 'PersonalCenter' });
    }
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
    margin: 10px;
  }
  ul {
    background-color: aqua;
  }
  ul li{
    list-style: none;
    font-size: 18px;
    padding: 5px;
    border: 1px solid #ddd;
    border-bottom: none;
  }
  ul li:hover{
    cursor: pointer;
    /* background-color: blue; */
    border-right: none;
  }
  .left-content{
    border-bottom: 1px solid #ddd;
    margin: 10px;
  }
  .demo-carousel{
    height: 230px;
    margin: 10px;
  }
  .show-container{
    border-top:1px solid #ddd;
    padding: 20px;
  }
  .img-size{
    width: 240px;
    height: 150px;
  }
</style>
