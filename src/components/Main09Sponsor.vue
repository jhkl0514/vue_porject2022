<template>
  <div class="wrap Main09Sponsor">
    <div class="container">
      <!-- {{Main09support}} -->      
      <div class="row">
        <div class="col-md-4 txt">
          <p>국내외 여러기업이 동참하고 있습니다.</p>
          <h2>JA Korea 후원</h2>
          <div class="btnMore">
                  <a href="#" class="btnMore01">
                    <span>자세히 보기</span>
                    <i class="fa-solid fa-arrow-right-long"></i>
                  </a>
          </div>
          <div class="paging d-flex gap-3 ">  
             <div class="prev"><i class="fa-solid fa-arrow-left-long"></i></div>
             <div class="next"><i class="fa-solid fa-arrow-right-long"></i></div>            
        </div>
        </div>

        <div class="col-md-8" style="height:400px">
          <swiper            
            :modules="modules2"
            v-bind="swiperOptions2" 
            class="mySwiper03"
          > 
            <swiper-slide  v-for="(item, i) in Main09support" :key="i">
              <div class="wrapImgBg">
              <div class="wrapImg">        
                 <img :src="`images/09support/${item.src}`" alt="">           
              </div>
              </div>
            </swiper-slide>
          </swiper>
        </div>
       
      </div>
    </div>
  </div>      
</template>
<script>
// Import Swiper Vue.js components
import { Swiper, SwiperSlide } from "swiper/vue";

// Import Swiper styles
import "swiper/css";

import "swiper/css/grid";
import "swiper/css/pagination";
import "swiper/css/navigation";


// import required modules
import { Grid, Pagination, Navigation } from "swiper";

export default {
  components: {
    Swiper,
    SwiperSlide,
  },
  setup() {
    return {
      modules2: [Grid, Pagination, Navigation],
       swiperOptions2:{
        slidesPerView:3,
        grid:{
              rows: 3,
            },
        spaceBetween:10,
        pagination:{
              clickable: true,
            },
        navigation:{
          nextEl:'.paging .next',
          prevEl:'.paging .prev',
        },   
      }

  
    };   
  },
   props :["Main09support"],
};
</script>
<style lang="scss">
.Main09Sponsor{
  margin-bottom: 240px;
  .swiper {
  width: 100%;
  height: 100%;
  margin-left: auto;
  margin-right: auto;
}
 .swiper-slide {
  height: calc((100% - 10%) / 3) !important;
 }

  .txt{
    p{
      font-weight: 600;
      font-size: 18px;
      line-height: 20px;
      color: #285F74;
    }
    h2{
      font-weight: 800;
      font-size: 45px;
      line-height: 51px;
      margin-bottom: 85px;
    }

    .btnMore{     
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
          color: #fff;
          background-image: linear-gradient( -45deg,#00a0af,#00c0ca, #008b9c,
        #28708b,#285f74, #22404d,#285f74,#28708b,
        #008b9c,#00c0ca,#00a0af) !important;
          animation: animate 1s linear infinite;
          opacity:1;       
               
          @keyframes animate {
            100%{opacity:1;
            background-image: linear-gradient( -45deg,#00a0af,#00c0ca, #008b9c,
          #28708b,#285f74, #22404d,#285f74,#28708b,
          #008b9c,#00c0ca,#00a0af) !important;  }
          }         
      }  
    }

    .paging{
      margin-top: 130px;
      color: #C9C9C9;
      font-size: 30px;
      font-weight: 100;
    }

  }
  .wrapImgBg{
      background: #f3f6f7;
      border-radius: 10px;
      .wrapImg{        
          position: relative;
          height: 100px;
          overflow: hidden;   
          img{              
              position: absolute;         
              top: 50%;
              left: 50%;
              transform: translate(-50%, -50%);
              object-fit: contain;                   
            }
       }
  }
}

</style>
