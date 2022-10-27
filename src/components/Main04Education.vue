<template>
  <div class="Main04Education">
    <div class="container">
      <div class="row">
        <div class="col d-flex title">
          <div class="col-4 "><h2>JA 교육 프로그램</h2></div>
          <div class="col-6 tapWrap">
            <div class="tap" @click="tab=1" :class="{active:tab==1}">진로취업</div>
            <div class="tap" @click="tab=2" :class="{active:tab==1}">경제금융</div>
            <div class="tap" @click="tab=3" :class="{active:tab==1}">기업가정신</div>
            <div class="tap" @click="tab=4" :class="{active:tab==1}">디지털 리터러시</div>
          </div>
          <div class="col-2"></div>
        </div>
      </div>

    </div>
  </div>
</template>

<script>
export default {
  components:{

  },
  props:[
 
  ],
  data(){
    return{
      tab:1,
    }
  }

}
</script>

<style lang="scss">
.Main04Education{
  .title{
    h2{
      font-weight: 800;
      font-size: 45px;
      color: #000000;
    }
    .tapWrap{
      display: flex;
      justify-content: space-between;
      padding-top: 18px;
      .tap{        
        font-size: 20px;
        color: #000000;
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
}

</style>