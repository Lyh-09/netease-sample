<template>
  <div class="home-container">
    <HeaderTitle/>
    <div class="home-main">
      <div class="home-content" style="padding-top: 74px">
        <SwiperImg/>    <!--轮播图-->
        <div class="servicePolicy">
          <ul>
            <li class="item">
              <a href="javascript:">
                <i class="iconfont icon-yi-copy"></i> <span class="text">网易自营品牌</span>
              </a>
            </li>
            <li class="item">
              <a href="javascript:">
                <i class="iconfont icon-icon-icon-duihao"></i> <span class="text">30天无忧退货</span>
              </a>
            </li>
            <li class="item">
              <a href="javascript:">
                <i class="iconfont icon-qian5"></i> <span class="text">48小时快速退款</span>
              </a>
            </li>
          </ul>
        </div>
        <Policy/>
        <Split/>
        <NewCouple/>
        <Split/>
        <CategoryModule/>
        <Split/>
        <LimitShop/>
        <Split/>
        <Recommend/>
        <Split/>
        <CrowdFunding/>
        <GoodList/>
        <HomeFooter/>
      </div>
    </div>
  </div>
</template>

<script type="text/ecmascript-6">
  import HeaderTitle from '../../components/HeaderTitle/HeaderTitle'  //头部搜索
  import SwiperImg from './components/Swiper/SwiperImg' //轮播图
  import Policy from './components/Policy/Policy'  //主导航区
  import NewCouple from './components/NewCouple/NewCouple'  //新人专享礼
  import CategoryModule from './components/CategoryModule/CategoryModule'  //商品模块
  import LimitShop from './components/LimitShop/LimitShop'  //限时购
  import Recommend from './components/Recommend/Recommend'  //人气推荐
  import CrowdFunding from './components/CrowdFunding/CrowdFunding' //众筹
  import GoodList from './components/GoodList/GoodList'  //物品列表
  import HomeFooter from './components/HomeFooter/HomeFooter'  //home底部

  import {mapState} from 'vuex'
  export default {
    components: {
      HeaderTitle,
      SwiperImg,
      Policy,
      NewCouple,
      CategoryModule,
      LimitShop,
      Recommend,
      CrowdFunding,
      GoodList,
      HomeFooter,
    },

    methods: {
      
    },

    computed: {
      ...mapState({
        homeData: state => state.home.homeData
      })
    },

    mounted() {
      
    },
  }
</script>

<style lang="stylus" rel="stylesheet/stylus">
  .home-container
    padding-bottom 47px
    .home-main
      .home-content
        .servicePolicy
          background-color #FFFFFF
          color $themeColor
          ul
            box-sizing border-box
            width 100%
            height 36px
            padding 0 15px
            display flex
            justify-content center
            li
              display flex
              justify-content center
              align-items center
              margin-right 10px
              a
                color $themeColor
                display flex
                justify-content center
                align-items center
                .iconfont
                  font-size 18px
                  margin-left 5px
                  color red
                .text
                  font-size 12px
                  margin-left 4px
                  line-height 16px
                  vertical-align middle
</style>
