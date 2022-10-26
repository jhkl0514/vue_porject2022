<template>  
  <!-- {{Main04Notice[0].name}}<br>
  {{Main05Story[0].name}}<br>
  {{Main06News[0].name}}<br> -->
  <div class="wrap Main07Notice">
    <div class="container">
      <div class="d-flex row mb-5">   
        <div class="col-6 col-md-3"><h2>기관소식</h2></div>
        <div class="NoticeTitle d-flex col-6  col-md-3">
          <div class="tab col col-md-4" @click="tab=1" :class="{active:tab==1}">공지사항</div>
          <div class="tab col col-md-4" @click="tab=2" :class="{active:tab==2}">스토리</div>
          <div class="tab col col-md-4" @click="tab=3" :class="{active:tab==3}">언론보도</div>
        </div>
      </div>

      <Main07TapSwiper :Main04Notice="Main04Notice" :Main05Story="Main05Story" :Main06News="Main06News" :tab="tab"></Main07TapSwiper>

    </div>
  </div>
</template>

<script>
import Main07TapSwiper from "@/components/Main07TapSwiper.vue"


export default {
  components:{
    Main07TapSwiper
  },
  props:[
    "Main04Notice",
    "Main05Story",
    "Main06News"
  ],
  data(){
    return{
      tab:1,
    }
  }

}
</script>

<style lang="scss">
.Main07Notice{  
    h2{
    font-weight: 800;
    font-size: 45px;
    }
    .NoticeTitle{
      display: flex; justify-content:space-between;
      gap:50px;
      >div{
        padding: 16px 0px 0px 0px;        
        font-size: 20px;
        position: relative;    
        text-align: center;
        cursor:pointer;      
        &:hover{
          font-weight: 800;
        }
        &.active{
          font-weight: 800;       
        &:after{
          content: ""; display: block;
          position: absolute;
          width: 100%;
          height: 4px; 
          background: #365A66;                   
        } 
         }       
        
         
      }
    }

}

</style>