<template>
  <div class="Main11Footer">
    <div class="wrapBg">
      <div class="container">
        <div class="row">      
            <ul class="fTxt col-md-6">
              <li><a href="#" class="bnt01">이용약관</a></li>
              <li class="pi"><a href="#">개인정보처리방침</a></li>
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
          <div class="col-md-4">
           <p class="snsFollow d-flex justify-content-end">Follow SNS</p>          
           <ul class="d-flex justify-content-end">
              <li class="fs-6  ms-3">
                  <a href="#"> <i class="fa-brands fa-facebook"></i></a>
                </li>
                <li class="fs-6 ms-3">
                  <a href="#"> <i class="fa-brands fa-instagram"></i></a>
                </li>
                <li class="fs-6 ms-3">
                  <a href="#"> <i class="fa-brands fa-youtube"></i></a>
                </li>
              </ul>         
          </div>
      </div>
    </div>

    <div class="container wrapCopy">
      <div class="row">
          <div class="footerLogo">
            <h2><a href="#"><img src="../assets/footer-logo.svg" alt=""></a></h2>
          </div>
          <div class="footerAddr">
            <p>서울특별시 강서구 양천로 583, B동 1408호(염창동, 우림블루나인비즈니스센터) 사단법인 제이에이코리아    우편번호 : 07547    대표 : 이은형    사업자번호 : 107-82-10367</p>
            <p>대표전화 : 02-783-2367    팩스 : 070-4275-5115    이메일 : jakorea@jakorea.org</p>
            <p class="py-2">ⓒJA Korea,2022</p>
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
        .pi{
              color: #285f74;
              font-weight: bold;
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
    :hover{
      color: #777;
    }   
    .snsFollow{
      font-weight: 400;
      font-size: 16px;
      line-height: 23px;
      color: #A0A0A0;
    }
    i{
      color: #BCBCBC;
      font-size: 18px;
    }
  }
  .wrapCopy{
    .footerLogo{
      max-width: 233px;
      opacity: 0.4;
      margin-bottom: 30px;
    }
    .footerAddr{
      font-weight: 400;
      font-size: 15px;
      line-height: 17px;
    }
  }
}


</style>