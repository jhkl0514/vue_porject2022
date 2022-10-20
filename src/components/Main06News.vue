<template>
  <div class="wrap Main06News">   
    <div class="container">
      <div class="row">
        <div class="col-12 col-md-6 pe-md-5">
          <!-- {{Main07notice}} -->
          <div class="newsTitle-wrap">
            <div class="board-top">
              <h2 class="title_01">모집공고</h2>
               <a href="#" class="btn_plus">
                <span><img src="../assets/btn_pluse.svg" alt=""></span>
               </a>
            </div>
            <div class="bg-dark mt-4 mb-4" style="height: 2px;"></div>
            <div class="board-li">
              <ul style="padding-left: 0rem;">
                <li v-for="(item, i) in 4" :key="i">
                  <div class="wrapBar board-bg">
                    <div class="d-flex">
                        <div class="board-title btn name" :class="{ing:Main07notice[i].name == '모집중'}">
                          {{ Main07notice[i].name }}
                        </div>
                        <div class="board-li-txt">
                            <strong class="fs-4 pb-4">{{ Main07notice[i].title }}</strong><br>
                            <span>{{ Main07notice[i].operate  }}</span>
                          </div>
                    </div>
                  </div>
                  <hr>
                </li>
              </ul>
            </div>
          </div>
       </div>

       <div class="col-12 col-md-6 ps-md-5">
          <!-- {{Main08result}} -->
          <div class="newsTitle-wrap">
            <div class="board-top">
              <h2 class="title_01">결과발표</h2>
               <a href="#" class="btn_plus">
                <span><img src="../assets/btn_pluse.svg" alt=""></span>
               </a>
            </div>
            <div class="bg-dark mt-4 mb-4" style="height: 2px;"></div>
            <div class="board-li">
              <ul style="padding-left: 0rem;">
                <li v-for="(item, i) in 4" :key="i">
                 
                    <div class="wrapBar board-bg">
                          <div class="board-li-txt">
                              <strong class="fs-4">{{ Main08result[i].title }}</strong><br>
                              <span>{{ Main08result[i].date  }}</span>
                           </div>
                    </div>
               
                  <hr>
                </li>
              </ul>
            </div>
          </div>
       </div>

      </div>
      </div>   
  </div>
</template>

<script>
export default {
props:[
  "Main07notice","Main08result"

]
}
</script>

<style lang="scss">
.Main06News{
  .newsTitle-wrap{
    .board-top{
      display: flex;
      justify-content: space-between;
      h2{
      font-size: 35px;
      font-weight: 700;
     }    
    }
    .board-li{
      .board-title{
        font-size: 14px;
        background: #2F3334;
        border-radius: 20px;
        width: 120px;
        height: 30px;
        padding: 5px 10px;
        color:#fff; 
        margin-right: 20px;
        &.ing{
          background:#285F74;
          width: 65px;
        }
      }
      .board-bg{
        padding: 30px 20px;
        cursor: pointer;
        &:hover{
          background: #FFFFFF;
          box-shadow: 0px 0px 15px rgba(0, 0, 0, 0.2);
          border-radius: 30px;
          transition: .3s;
        }
        strong{ 
            display: block;           
            overflow: hidden;
            text-overflow: ellipsis;       
            height: 32px;
            width: 100%;                     
        }        
      } 
    }    
   
     }
    
  }


</style>