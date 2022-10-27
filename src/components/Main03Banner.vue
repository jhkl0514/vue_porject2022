<template>
 <div class="wrap Main03Banner">
    <div class="container">
      <!-- {{Main03Banner}} -->
      <div class="row">       
          <div class="quick-li col-md col-6"  v-for="(item, i) in Main03Banner" :key="i" :class="{'d-none d-md-block':i==4}">
            <div class="quick-menu">
                  <a :href="Main03Banner[i].href">
                    <div>
                      <img :src="`images/02iconBanner/${item.src}`" alt="">
                    </div>
                    <strong>{{Main03Banner[i].title}}</strong>
                    <p>{{Main03Banner[i].subtitle}}</p>
                  </a>
                </div>
          </div>
      </div>

    </div>
</div>
</template>

<script>
export default {
  props:["Main03Banner"]
}
</script>

<style lang="scss">
.Main03Banner{
  margin-bottom: 200px;
  .quick-li{
    display: flex;
    justify-content: space-between;
    .quick-menu{
    a{
      display: block;
      width: 100%;
      text-align: center;
      padding:40px 25px;
      div{
        	height:170px;
          position:relative;
          top:0;
          transition:.4s;
          img {
              height: 140px;
              text-align: center;
          }
      }
      strong {
        font-size:18px;
          font-family: "NanumSquareEB";
      }
      p {
        margin-top: 14px;
        font-size: 15px;
        line-height: 1.6;
        word-break: keep-all;
      }
    }
    a:hover{
      	top:-20px;
        div {
	      top:-20px;
      }
    }
    
  }
  }

  
}

</style>