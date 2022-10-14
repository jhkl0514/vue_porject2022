<template>
  <div class="wrap" style="background:#E1F0F1; height:745px">
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
          <swiper-slide v-for="(item,i) in swiperView" :key="i">
            <div class="innerItem video col-lg-8 position-relative mb-3 mb-lg-0">              
              <!-- {{swiperView[0].subtitle}} -->
              <video autoplay muted loop playsinline preload="metadata" style="" class="img-fluid">
                    <source :src="`./images/01mainSlide_video/${item.mVideo}`" type="video/mp4">
              </video>
            </div>
          </swiper-slide>
        </swiper>
      </div>
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

//swiper data
import sData from "@/data/01mainSlide.js"

export default {
  components: {
    Swiper,
    SwiperSlide,
  },
  setup() {
    return {
      modules: [Pagination, Navigation],
      swiperView:sData,
    };
  },
};
</script>
<style lang="scss">
.mySwiper .swiper-slide{
    height: 650px;
    overflow: hidden;
    .innerItem{height: 100%;}
    video{display: block;margin: 0 auto;}    
   
}

  


</style>