<template>
  <div class="Main10Newsletter">
    <div class="container">
      <div class="row">
        <div class="wrapNL">
          <h3>JA Korea 뉴스레터 구독하기</h3>
          <div class="inpBox row d-flex">
            <div class="col-md-3 input">
              <i class="far fa-user"></i> 
              <input type="text" name="name" id="" placeholder="이름"/>
            </div>
            <div class="col-md-3 input">
              <i class="far fa-envelope"></i> 
              <input type="text" name="e-mail" id="" placeholder="이메일"/>            
              </div>
            <div class="col-md-6 btn" >
              신청하기             
            </div>  
            
          </div>
          <div class="chack d-flex gap-2">
            <i class="fa-regular fa-circle-check"></i>
            <p>뉴스레터 구독을 위한 이름 및 이메일 주소 수집에 동의합니다.</p>
          </div>          
        </div>
        <div class="imgMan d-none d-md-block">
            <img src="../assets/subscribe-img.png" alt="">          
          </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss">
.Main10Newsletter {
  position: relative;
  margin-bottom: 170px;
  .wrapNL {
    overflow: hidden;
    position: relative;
    background: linear-gradient(90.12deg, #059fab 0.1%, #00bdc9 92.71%);
    border-radius: 20px;
    padding: 50px;
    h3 {
      color: white;
      font-weight: 800;
      font-size: 30px;
      line-height: 34px;
      margin-bottom: 25px;
    }
    .chack {
      font-weight: 400;
      font-size: 18px;
      line-height: 20px;
      i {
        color: rgba(0, 0, 0, 0.5);
        padding: 0 0 0 0;
        font-size: 22px;
        cursor: pointer;
        &:hover{
          color:white;
        }
      }
      p {
        color: white;
      }
      }
    .inpBox{
      gap:10px;
      margin-bottom: 20px;
      .input{         
          height: 70px;       
          border-radius: 10px;
          border: none;
          background-color: #35C0C9;
          padding: 0 50px 0 30px;
          color: #fff;
          font-size: 18px;
          overflow:hidden;  
          display: flex;   
          align-items: center;
          gap:10px;
          input{
            background-color: #35C0C9;
            border: #35C0C9;
            color: #fff;
            font-size: 18px;
            overflow:hidden;
            text-overflow:ellipsis;
            padding: 10px 0;
            &:focus {
              outline: none;
            }
            &::placeholder {
              font-weight: 400;
              color: white;
            }
          }
      }
      .btn{
        width: 150px;        
        height: 68px;       
        border: 1px solid #FFFFFF;
        border-radius: 10px;
        color:white;
        line-height: 50px;
        &:hover{
          background: white;
          color:#333
        }
      }
    }  
    
  }
  .imgMan{
      position: absolute; 
      width: 400px;  
      right: 200px;
      top: -35px;
      z-index: 100;
      img{
      width: 350px;

      }
    }
}
</style>