<template>
  <div class="TapSwiper ">
      <swiper
         v-bind="swiperOptions1"
        :modules="modules1"
        class="mySwiper1"
      >

        <swiper-slide v-if="tab==1" v-for="item in Main04Notice" :key="item" :class="{Main04Notice:tab=1}">         
             <h4>{{item.name}}</h4>
             <h5>{{item.title}}</h5>
             <p>{{item.subtitle}}</p>    
        </swiper-slide>
        
        <swiper-slide v-if="tab==2" v-for="item in Main05Story" :key="item" :class="{Main05Story:tab=2}">
            <h4>{{item.name}}</h4>
            <h5>{{item.title}}</h5>
            <p>{{item.subtitle}}</p>
        </swiper-slide>
        <swiper-slide v-if="tab==3" v-for="item in Main06News" :key="item" :class="{Main06News:tab=3}">
            <h4>{{item.name}}</h4>
            <h5>{{item.title}}</h5>
            <p>{{item.subtitle}}</p>
        </swiper-slide>      
      </swiper>
      <div class="btnWrap">
          <div class="prev"><i class="fa-solid fa-arrow-left-long"></i></div>
          <div class="next"><i class="fa-solid fa-arrow-right-long"></i></div>
      </div>
  </div>

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

export default {
  components: {
    Swiper,
    SwiperSlide,
  },
  props:[
    "Main04Notice", "Main05Story", "Main06News", "tab"  
  ],
  setup() {
    return {
      modules1: [Pagination, Navigation],
      swiperOptions1:{
        slidesPerView:1,
        spaceBetween:0,
         breakpoints: {
          // 1280px 보다 클 경우
          1280: {
            slidesPerView: 3,
            spaceBetween: 30
          }
         },
        loop:true,
        observer: true,
        observeParents: true,
        navigation:{
          nextEl:'.btnWrap .next',
          prevEl:'.btnWrap .prev',
        },
      }
    };
  },
};
</script>
<style lang="scss">
.TapSwiper{
    padding: 20px 80px;
    position: relative;    
    .swiper-slide{      
        height: 400px; 
        margin: 0px;       
        &.Main04Notice{
            // background: #eee;
        }
        &.Main05Story{
            // background: pink;
        }
        &.Main06News{
            // background: green;
        }
        h4{
            background: #000000;
            border-radius: 20px;
            color: #fff;
            display: block;
            font-weight: 400;
            font-size: 14px;
            display:inline-block;
            padding: 8px 15px;
            margin: 1px;
          
        }
        h5{
            font-weight: 700;
            font-size: 24px;          
            word-wrap: break-word;
            -webkit-line-clamp: 3;
            -webkit-box-orient: vertical;
            overflow: hidden;
            text-overflow: ellipsis;
            line-height: 34px;
            height: 90px;
            padding: 20px 0 14px 0;
        }
        p{
            font-size: 18px;      
            word-wrap: break-word;
            -webkit-line-clamp: 3;
            -webkit-box-orient: vertical;
            overflow: hidden;
            text-overflow: ellipsis;
            line-height: 31px;
            height: 96px;
            margin-top: 28px;
        }
        
    }
    .btnWrap{     
      display: flex;
      z-index: 20;
      gap:10px;
      left: calc( 50% + 300px);
      .next,.prev{
            position: absolute;
            background: #FFFFFF;
            box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.1);
            border-radius: 28px;
            top: 120px;
            color: #149197;
            width: 65px;
            height: 56px;       
            font-size: 18px; 
            display: flex;
            justify-content: center;
            align-items: center;   
            cursor:pointer;
      }
      .prev{
        position: absolute;
        left: -25px;
        right: auto;
        z-index: 10;
      }
      .next{
        position: absolute;
        right: -25px;
        left: auto;
        z-index: 10;
      }
    }
}
// $small: 768px;
// @media screen and (max-width: $small) {
//   .TapSwiper{ 
//     .swiper-slide{
//       background: pink; 
//        width: 500px;          
//     }        
// }
// }
</style>
  