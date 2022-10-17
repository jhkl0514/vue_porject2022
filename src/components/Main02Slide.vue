<template>
  <div class="wrap Main02Slide" style="background: #e1f0f1; height: 745px">
    <div class="container">
      <div class="row">
        <swiper
          :slidesPerView="1"
          :spaceBetween="30"
          :loop="true"
          :pagination="{
            clickable: true,
          }"
          :navigation="true"
          :modules="modules"
          class="mySwiper"
        >
          <swiper-slide v-for="(item, i) in Main02Slide" :key="i">
            <div  class="innerItem video mb-3 mb-lg-0">
              <!-- {{swiperView[0].subtitle}} -->
              <div class="video_txt col-md-6">
                <h3 v-html="item.mainTitle"></h3>
                <p  v-html="item.subtitle"></p>
              </div>

              <div class="video01 col-md-6" :class="`video_${i}`">
                <video  autoplay  muted loop playsinline  preload="metadata" style="" class="img-fluid">
                  <source :src="`./images/01mainSlide_video/${item.mVideo}`" type="video/mp4">
                </video>
              </div>
            </div>
          </swiper-slide>
        </swiper>
        <div class="btnWrap">
          <div class="prev">이전</div>
          <div class="next">다음</div>
        </div>
      </div>
    </div>
  </div>
  <!-- {{Main02Slide}} -->
</template>
<script>
// Import Swiper Vue.js components
import { Swiper, SwiperSlide } from "swiper/vue";

// Import Swiper styles
import "swiper/css";

import "swiper/css/pagination";
import "swiper/css/navigation";

// import required modules
import { Pagination, Navigation } from "swiper";

//swiper data
// import sData from "@/data/01mainSlide.js"

export default {
  components: {
    Swiper,
    SwiperSlide,
  },
  setup() {
    return {
      modules: [Pagination, Navigation],
      // swiperView:sData,
      swiperOptions:{
        loop:true,
        navigation:{
          nextEl:'.Main02Slide .next',
          prevEl:'.Main02Slide .prev',
        },
        pagination:{
          // clickable:true
          type:'fraction'
          }
      }
    };
  },
  props: ["Main02Slide"],
  //데이터받기
};
</script>
<style lang="scss">
.wrap {
  &.Main02Slide {
    position: relative;
    .mySwiper .swiper-slide {
      height: 650px;
      overflow: hidden;
      .innerItem {
        height: 100%;
        position: relative;
        display: flex;
        align-items: center; 
        .video01 {
          position: absolute;
          display: flex;justify-content: flex-end;
          right: 0;       
          bottom: 0;
          width: 1000px;
          height: 100%;
          padding-top: 120px;
        }
      }
      video {
        display: block;       
      }
      .video_0{
        video{width: 60%;}
      }
      .video_1{
        video{width: 80%;}
      }
      .video_txt {
        z-index:1;       
        width:67%;
        font-family: 'NanumSquare';  
        color: #285E76;     
                   
        strong{
          font-size:66px; 
          font-weight: 300;
          b{
            font-weight: 800;
          }
        }
        p {
          font-weight: 700;
          font-size: 18px;
          line-height: 22px;          
        }
      }
    }
    .btnWrap{
      position: absolute;
      display: flex;
      bottom: 20px;
      z-index: 10;
      gap:10px;
      left: calc( 50% + 300px);
      .next,.prev{
        padding: 5px 10px;
        background: rgba(0,0,0,0.3);
        border-radius: 10px;
        color: white;
        cursor:pointer;
      }
    }
  }
}
</style>