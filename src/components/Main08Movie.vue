<template>
  <div class="rwap Main08Movie">
        <div class="Main08_video"> 
              <div class="txtWrap">
                    <div class="container">                                    
                      <div class="title">
                        <div class="video-title">
                            우리 청소년들이 미래의 인재로 성장하도록
                        </div>
                        <div class="video-subtitle">
                          JA KOREA가 함께합니다.
                        </div>                        
                      </div>

                      <div class="btnMore">
                          <a href="#" class="btnMore01">
                            <span>자세히 보기</span>
                            <i class="fa-solid fa-arrow-right-long"></i>
                          </a>
                    </div>

                    </div>                    
              </div>

              <div class="wrapVideo">
                <video muted loop autoplay playsinline preload="metadata" poster="" id="mainVdo" class="mainvdo">
                      <source src="../assets/main-home-01-2.mp4" type="video/mp4">
                </video>
              </div>         
        </div>        
  </div>
</template>


<script>
export default {

}
</script>

<style lang="scss">
.Main08Movie{
  .Main08_video{
    width: 100%;
    height: 100vh;
    position: relative;
    display: flex;justify-content: center;align-items: center;
    overflow: hidden;
    margin-bottom: 180px;
  }
  .txtWrap{
    width: 100%; 
    position: absolute;
    top:0;
    left:0;
    padding: 15% 8%;   
    
    .title{
      .video-title{
      font-weight: 200;
      font-size: 38px;
      line-height: 60px;
      color: #FFFFFF;
      background: #00BEC6;
      display: inline-block;    
      padding: 0 10px;
      }
      .video-subtitle{
        font-weight: 800;
        font-size: 75px;
        line-height: 120px;
        color: #FFFFFF;
        margin-bottom: 90px;
      }
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
  .wrapVideo{
    padding-top:60%; 
    .mainvdo{
      position: absolute;
      right:0;
      bottom: 0;
      object-fit: cover;
      z-index: -1;
    }
  }

}
@media (min-aspect-ratio: 16/9){
  .mainvdo{
    width: 100%;
    height: auto;
  }
}
@media (max-aspect-ratio: 16/9){
  .mainvdo{
    width: auto;
    height: 100%;
  }
}

$small: 768px;
@media screen and (max-width: $small) {
  .txtWrap{
    padding: 50% 8% !important; 

  .title{
      .video-title{     
      font-size: 20px !important; 
      padding: 0 5px !important; 
   
      }
      .video-subtitle{
        font-weight: 800;
        font-size: 35px !important;
        line-height: 80px !important;
      }
    }
  }
}
</style>