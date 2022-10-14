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
  *{margin: 0;padding: 0;}
  ul,li{list-style: none;}
  a:link,a:visited{text-decoration: none;color: #333;}
  .container{width: 1280px;margin: 0 auto;}
</style>