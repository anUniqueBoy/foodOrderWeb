<template>
  <div class="container">
    <div class="header">
      <div class="header-search">
        <Input v-model="search" icon="ios-search-strong" placeholder="Enter something..." style="width: 400px;"></Input>
        <Button type="info">搜 索</Button>
      </div>
      <div class="header-people" @click="jumpPeosonalCenter">
        <div style="width:30px;height:30px;">
          <img src="../assets/personCenter.png" alt="" style="width:100%;height:100%;vertical-align:middle">
        </div>
        <p style="margin-left:5px;color:#fff">个人中心</p>
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
      <Row :gutter="24">
        <Col span="6">
          <div class="item" @click="jumpDetail">
            <div>
              <img class="img-size" src="../assets/timg (2).jpg" alt="">
            </div>
            <div style="text-align:left">
              <span class="font-span">￥20</span>
              <p class="font-p">铁板培根饭</p>
            </div>
          </div>
        </Col>
        <Col span="6">
          <div class="item">
            <div>
              <img class="img-size" src="../assets/timg (1).jpg" alt="">
            </div>
            <div style="text-align:left">
              <span class="font-span">￥20</span>
              <p class="font-p">铁板培根饭</p>
            </div>
          </div>
        </Col>
        <Col span="6">
          <div class="item">
            <div>
              <img class="img-size" src="../assets/timg (3).jpg" alt="">
            </div>
            <div style="text-align:left">
              <span class="font-span">￥20</span>
              <p class="font-p">铁板培根饭</p>
            </div>
          </div>
        </Col>
        <Col span="6">
          <div class="item">
            <div>
              <img class="img-size" src="../assets/timg (4).jpg" alt="">
            </div>
            <div style="text-align:left">
              <span class="font-span">￥20</span>
              <p class="font-p">铁板培根饭</p>
            </div>
          </div>
        </Col>
        <Col span="6">
          <div class="item">
            <div>
              <img class="img-size" src="../assets/timg (1).jpg" alt="">
            </div>
            <div style="text-align:left">
              <span class="font-span">￥20</span>
              <p class="font-p">铁板培根饭</p>
            </div>
          </div>
        </Col>
        <Col span="6">
          <div class="item">
            <div>
              <img class="img-size" src="../assets/timg.jpg" alt="">
            </div>
            <div style="text-align:left">
              <span class="font-span">￥20</span>
              <p class="font-p">铁板培根饭</p>
            </div>
          </div>
        </Col>
        <Col span="6">
          <div class="item">
            <div>
              <img class="img-size" src="../assets/timg (4).jpg" alt="">
            </div>
            <div style="text-align:left">
              <span class="font-span">￥20</span>
              <p class="font-p">铁板培根饭</p>
            </div>
          </div>
        </Col>
        <Col span="6">
          <div class="item">
            <div>
              <img class="img-size" src="../assets/timg (3).jpg" alt="">
            </div>
            <div style="text-align:left">
              <span class="font-span">￥20</span>
              <p class="font-p">铁板培根饭</p>
            </div>
          </div>
        </Col>
      </Row>
    </div>
    <div class="footer">
      <Page :total="100" show-total></Page>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Home',
  data () {
    return {
      search: '',
      value: 0,
    }
  },
  mounted() {
  },
  methods: {
    jumpPeosonalCenter() {
      this.$router.push({ name: 'PersonalCenter' });
    },
    jumpDetail() {
      this.$router.push({ name: 'Detail' });
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
    background-color: #545051;
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
  .left-content {
    background:transparent;
    background-color: #174369;
    color: #fff;
    opacity: 0.8;
  }
  .left-content li{
    list-style: none;
    font-size: 18px;
    padding: 5px;
    border-bottom: none;
  }
  ul li:hover{
    cursor: pointer;
    background-color: #fff;
    color: #545051;
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
    padding: 20px 20px 0;
  }
  .img-size{
    width: 100%;
    height: 150px;
  }
  .font-p{
    font-size: 20px;
    padding:0 10px;
    display: inline;
  }
  .font-span{
    padding:0 10px;
    font-size:22px;
    color: #e4393c;
  }
  .item {
    margin-bottom: 20px;
    cursor: pointer;
  }
  .footer{
    text-align: right;
    margin: 0 20px 20px 20px;
  }
</style>
