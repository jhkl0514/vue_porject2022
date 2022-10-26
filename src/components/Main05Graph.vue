<template>
  <section class="wrap Main05Graph" id="graphGradient">
    <div class="container d-flex">
      <div class="row col">

      <div class="col col-md-4 d-flex align-items-center">
        <div class="graph-img mt-5 mt-md-0 ">
          <img src="../assets/main-number-1.jpg" alt="" />
        </div>
      </div>

      <div class="col col-md-8 mt-5 mb-4">
        <ul class="graph-li">
          <li>
            <div class="graph-li-top">
              <div class="graph-li-bar"><span></span></div>
              <p class="num">+200</p>
            </div>
            <div class="box">
              <strong>지역 네트워크</strong>
              <p>전국 17개 시도 200개이상의 지역에서 교육하고 있습니다.</p>
            </div>
          </li>
          <li>
            <div class="graph-li-top">
              <div class="graph-li-bar"><span></span></div>
              <p class="num">+1,000</p>
            </div>
            <div class="box">
              <strong>학교 및 기관</strong>
              <p>
                전국 1,000여개 학교 및 기관, 단체와 협업하여 교육을 진행합니다.
              </p>
            </div>
          </li>
          <li>
            <div class="graph-li-top">
              <div class="graph-li-bar"><span></span></div>
              <p class="num">+3,000</p>
            </div>
            <div class="box">
              <strong>교육 진행자</strong>
              <p>
                3,000여명의 전문 지식을 갖춘 봉사자와 교사, 강사가 함께 교육을
                진행하고 있습니다.
              </p>
            </div>
          </li>
          <li>
            <div class="graph-li-top">
              <div class="graph-li-bar"><span></span></div>
              <p class="num">+90,000</p>
            </div>
            <div class="box">
              <strong>교육 수혜자</strong>
              <p>전국 90,000여명의 청소년들이 교육 프로그램에 참여합니다.</p>
            </div>
          </li>
        </ul>
      </div>

      </div>
    </div>
  </section>
</template>

<script>
export default {};
</script>

<style lang="scss">
.Main05Graph{
  _height: 470px;
  background: linear-gradient(89.94deg, #244B69 5.99%, #196673 100.79%);
  margin-bottom: 200px;
  .graph-img{   
    img{      
    border-radius: 30px;
    width: 400px;   
    background: pink;
    }
  }
  .graph-li{
    padding: 20px 0;
    li{
      margin-bottom: 10px;
    }
    .graph-li-top{
      display: flex;
      _justify-content:flex-start;
      align-items: center;
      .num{
        font-size:30px;
        color: white;
        font-weight: 800;
        line-height: 10px;
        font-family: "NanumSquareB";
      }
      .graph-li-bar{
      display: flex;
      align-items: center;
      height: 10px;
      background: rgba(255, 255, 255, .5);
      border-radius: 5px;
      position: relative;
      margin-right: 15px;
      width: 75%;
      _display: inline-block;
      span{
      display: block;
      height: 100%;
      width: 70%;
      position: absolute;
      top: 0;
      left: 0;
      _background: #fff;
      border-radius: 5px;
      background:#00a0af;
      }
    }
    }
  .box{
    display: flex;
    strong{
      font-weight: 7oo;
      color: #fff;
      font-size:16px;
      margin-right: 10px;
      flex-shrink:0;
    }
    p{
      color: rgba(255, 255, 255, .5);
      font-size:14px;
    }
  }  
  }
  
}
</style>