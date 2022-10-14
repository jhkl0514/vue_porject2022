<template>
  <MainMenu></MainMenu>
  <MainSlide></MainSlide>
  <MainBanner></MainBanner>
  <MainEducation></MainEducation>
  <MainGraph></MainGraph>
  <MainNews></MainNews>
  <MainNotice></MainNotice>
  <MainMovie></MainMovie>
  <MainSponsor></MainSponsor>
  <MainNewsletter></MainNewsletter>
  <MainFooter></MainFooter>

</template>

<script>
import MainMenu from "@/components/Main01Menu.vue"
import MainSlide from "@/components/Main02Slide.vue"
import MainBanner from "@/components/Main03Banner.vue"
import MainEducation from "@/components/Main04Education.vue"
import MainGraph from "@/components/Main05Graph.vue"
import MainNews from "@/components/Main06News.vue"
import MainNotice from "@/components/Main07Notice.vue"
import MainMovie from "@/components/Main08Movie.vue"
import MainSponsor from "@/components/Main09Sponsor.vue"
import MainNewsletter from "@/components/Main10Newsletter.vue"
import MainFooter from "@/components/Main11Footer.vue"


export default {
  components: {
    MainMenu,
    MainSlide,
    MainBanner,
    MainEducation,
    MainGraph,
    MainNews,
    MainNotice,
    MainMovie,
    MainSponsor,
    MainSponsor,
    MainNewsletter,
    MainFooter,
  },
}
</script>

<style>
@import url('https://cdn.rawgit.com/moonspam/NanumSquare/master/nanumsquare.css');
  *{margin: 0;padding: 0; }
  body{font-family: 'NanumSquare',san-serif; font-size:17px; line-height:1.5;}
  ul,li{list-style: none;}
  a:link,a:visited{text-decoration: none;color: #333;}
  .container{width: 1280px;margin: 0 auto;}
  .nanumsquare {font-family: 'NanumSquare', sans-serif !important;}
  .fontL{font-weight: 300;}
  .fontR{font-weight: 400;}
  .fontB{font-weight: 700;}
  .fontEB{font-weight: 800;}
</style>