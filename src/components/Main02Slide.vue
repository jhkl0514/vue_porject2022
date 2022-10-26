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
          v-bind="swiperOptions"          
          class="mySwiper"          
        >
        <!-- v-bind="swiperOptions" : Pagination, Navigation 바인드해줌 -->
          <swiper-slide v-for="(item, i) in Main02Slide" :key="i">
            <div  class="innerItem video mb-3 mb-lg-0">
              <!-- {{swiperView[0].subtitle}} -->
              <div class="video_txt col-md-6">
                <h3 v-html="item.mainTitle"></h3>
                <p  v-html="item.subtitle" class="mb-5"></p>
                <div class="btnMore">
                  <a href="#" class="btnMore01">
                    <span>자세히 보기</span>
                    <i class="fa-solid fa-arrow-right-long"></i>
                  </a>
              </div>
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
          <div class="prev"><i class="fa-solid fa-angle-left"></i></div>
          <div class="next"><i class="fa-solid fa-angle-right"></i></div>
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
          clickable:true
          // type:'fraction'
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
      _position: absolute;
      display: flex;
      _bottom: 20px;
      z-index: 10;
      gap:10px;
      left: calc( 50% + 300px);
      .next,.prev{
            color: #333;
            opacity: .4;
            font-size: 20px;
            transition: .3s;
        // padding: 5px 10px;
        // background: rgba(0,0,0,0.3);
        // border-radius: 10px;
        // color: white;
        cursor:pointer;
      }
    }
    .btnMore{
      position: absolute;      
      left:3px;
      a.btnMore01{
        padding: 20px 35px;
        border-radius: 40px;
        overflow: hidden;
        display: inline-block;
        background: #fff;       
        box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.15);
        transition: 0.3s;
        span {
          font-family: 'NanumSquare';         
          font-size: 17px;
          font-weight: 700;
          padding-right:48px ;       
        }       
      }
      a.btnMore01:hover{        
          box-shadow: 0 0 17px 6px rgba(0, 0, 0, 0); 
          background: linear-gradient(90deg, #00BDC8 2.33%, #008B9C 100%) !important;
          span{
            color:#fff;
          }
          i{
            color:#fff;
          }             
      }  
    }
  } 
  
}
$small: 768px;
@media screen and (max-width: $small) {
  .mySwiper{
    .video_txt {
      padding: 10px;
      position: absolute;
      top:20px;
      width:100% !important;                                      
        strong{
          font-size:40px !important;                  
        }
        p{
          font-size:14px !important; 
        }
       
      }
    .btnMore{ 
      position: absolute;
      top:550px;   
      a.btnMore01{
        padding: 10px 20px !important;  
        span {
          font-family: 'NanumSquare';         
          font-size: 12px  !important;  
          font-weight: 700;
          padding-right:48px ;       
        }       
      }  
    }  
  }
}



</style>