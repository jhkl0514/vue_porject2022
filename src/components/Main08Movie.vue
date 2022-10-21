<template>
  <div class="rwap Main08Movie">
      <div class="col">
        <div class="Main08_video">
          <video class="mainvdo" muted loop autoplay playsinline preload="metadata" poster="" id="mainVdo">
                <source src="../assets/main-home-01-2.mp4" type="video/mp4">
          </video>
        </div>
        <div class="txtWrap">
            <div class="video-title">
                    <ul>
                        <li>JA KOREA가 함께합니다.</li>
                    </ul>
                </div>
                <div class="video-subtitle">
                        <p class="">우리 청소년들이 미래의 인재로 성장하도록</p>
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

.Man08Movie{
  .Main08_video{
    width: 100%;
    padding-top: 60%;
    position: relative;
    overflow: hidden;
  }
  .mainvdo{
    position: absolute;
    top:0;
    left: 0;
    object-fit: cover;
  }

}
</style>