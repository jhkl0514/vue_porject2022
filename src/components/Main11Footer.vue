<template>
  <div class="Main11Footer">
    <div class="wrapBg">
      <div class="container">
        <div class="row">      
            <ul class="fTxt col-md-6">
              <li><a href="#" class="bnt01">이용약관</a></li>
              <li><a href="#">개인정보처리방침</a></li>
              <li><a href="#">이메일수집거부</a></li>
              <li><a href="#">오시는길</a></li>             
            </ul>  
          <div class="fFamily col-md-6 d-flex justify-content-end">
            <select class="family-site">
              <option>관련 사이트 보기</option>
              <option>JA Worldwide</option>
              <option>JA Africa</option>
              <option>JA Americas</option>
              <option>JA Asia Pacific</option>
            </select>
            <div class="down"><i class="fa-solid fa-angle-down"></i></div>
          </div>
        </div>
      </div>
    </div>

    <div class="container wrapFooter">
      <div class="row">
          <div class="col-md-8 d-flex gap-4">
            <p><a href="#">후원하기</a></p>
            <p><a href="#">온라인 학습관리</a></p>
            <p><a href="#">기부금영수증</a></p>
            <p><a href="#">국세청 공시 및 공개 내역</a></p>
            <p><a href="#">1:1문의</a></p>
          </div>
          <div class="col-md-4  bg-info">
           <p>Follow SNS</p>          
           <ul class="d-flex">
              <li class="fs-6  ms-3">
                  <a href="#"> <i class="fa-brands fa-facebook"></i></a>
                </li>
                <li class="fs-6 ms-3">
                  <a href="#"> <i class="fa-brands fa-instagram"></i></a>
                </li>
                <li class="fs-6 ms-3">
                  <a href="#"> <i class="fa-brands fa-facebook"></i></a>
                </li>
              </ul>         
          </div>
      </div>
    </div>
    


  </div>
</template>

<script>
export default {

}
</script>

<style lang="scss">
.Main11Footer{
  margin-bottom: 50px;
  .wrapBg{
    background: #F6F6F6;
    margin-bottom: 20px;
    .row{
      padding: 30px 0px 15px 0px;  
    .fTxt{
      display: flex;
      gap:20px;
      font-weight: 400;
      font-size: 17px;
      line-height: 19px;
        :hover{
          color: #285F74;
          font-weight: 700;
        }
      }
    .fFamily{ 
      position: relative;
      .family-site{        
        background: #fff;
        border-radius: 14px;
        border: 0;
        padding: 12px 20px;
        width: 237px;
        text-align: left;
        font-size: 14px;
        color: #333;
        z-index: 1; 
      }  
      .down {
          position: absolute; 
          top: 10px; 
          right: 15px;
          padding: 0 10px; 
          z-index: 10;
          background: white;
        i{        
          font-size: 18px;       
      
      
        }
      }
    }
    }
  }
  .wrapFooter{   
    background: pink;
  }
}


</style>