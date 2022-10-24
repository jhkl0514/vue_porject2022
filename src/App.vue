<template>
  <MainMenu></MainMenu>
  <MainSlide  v-bind:Main02Slide="Main02Slide"></MainSlide>
  <MainBanner v-bind:Main03Banner="Main03Banner"></MainBanner>
  <MainEducation></MainEducation>
  <MainGraph></MainGraph> 
  <MainNotice :Main04Notice="Main04Notice" :Main05Story="Main05Story" :Main06News="Main06News"></MainNotice>
  <MainNews :Main07notice="Main07notice" :Main08result="Main08result"></MainNews>
  <MainMovie></MainMovie>
  <MainSponsor :Main09support="Main09support"></MainSponsor>
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

import Main02Slide from "@/data/01mainSlide.js";
import Main03Banner from "@/data/02iconBanner.js";
import Main04Notice from "@/data/04notice.js"
import Main05Story from "@/data/05story.js"
import Main06News from "@/data/06news.js"
import Main07notice from "@/data/07notice.js"
import Main08result from "@/data/08result.js"
import Main09support from "@/data/09support.js"


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
    MainNewsletter,
    MainFooter,
  },
  data(){
    return {
    Main02Slide:Main02Slide,
    Main03Banner:Main03Banner,
    Main04Notice:Main04Notice,
    Main05Story:Main05Story,
    Main06News:Main06News,
    Main07notice:Main07notice,
    Main08result:Main08result,
    Main09support:Main09support,

    }
  }
}
</script>

<style>
@import url('https://cdn.rawgit.com/moonspam/NanumSquare/master/nanumsquare.css');
  *{margin: 0;padding: 0; }
  body{font-family: 'NanumSquare',san-serif !important; font-size:17px; line-height:1.5; }
  ul,li{list-style: none;}
  a:link,a:visited {text-decoration: none; color: #333 !important;}
  .container{width: 1280px;margin: 0 auto;}
  .nanumsquare {font-family: 'NanumSquare', sans-serif !important;}
  .fontL{font-weight: 300;}
  .fontR{font-weight: 400;}
  .fontB{font-weight: 700;}
  .fontEB{font-weight: 800;}
</style>