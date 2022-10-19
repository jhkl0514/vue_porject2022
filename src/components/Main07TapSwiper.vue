<template>
  <div class="TapSwiper col">
      <swiper
        ref="{swiperRef}"
        :navigation="true"
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
          <div class="prev"><i class="fa-solid fa-angle-left"></i></div>
          <div class="next"><i class="fa-solid fa-angle-right"></i></div>
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
      modules: [Pagination, Navigation],
      swiperOptions1:{
        slidesPerView:3,
        spaceBetween:30,
        loop:true,
        observer: true,
        observeParents: true,
        navigation:{
          nextEl:'.Main04Notice .next',
          prevEl:'.Main04Notice .prev',
        },
      }
    };
  },
};
</script>
<style lang="scss">
.TapSwiper{
    padding: 0px 40px;
    position: relative;    
    .swiper-slide{      
        height: 400px;        
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
            font-size: 16px;
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
      z-index: 10;
      gap:10px;
      left: calc( 50% + 300px);
      .next,.prev{
            position: absolute;
            top: 120px;
            color: #333;
            opacity: .4;
            font-size: 50px;
            transition: .3s;        
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
</style>
  