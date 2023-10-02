<template>
  <div class="overflow-hidden">
    <div class>
      <img
        src="@/assets/images/Vector 1.png"
        class="sm:absolute sm:block hidden right-0 top-0 w-[35%] lg:h-[650px] md:h-[620px] sm:h-[400px]"
        alt
      />
    </div>

    <NavBar></NavBar>
    <GetStarted></GetStarted>
    <OurBusiness></OurBusiness>
    <AboutUs></AboutUs>
    <RecentWork></RecentWork>
    <OurTestimonials></OurTestimonials>
    <Footer></Footer>
  </div>
</template>
<script>
import NavBar from "@/views/sections/sectionOne/NavBar.vue";
import GetStarted from "@/views/sections/sectionTwo/GetStarted.vue";
import OurBusiness from "@/views/sections/sectionThree/OurBusniness.vue";
import AboutUs from "@/views/sections/sectionFoor/AboutUs.vue";
import RecentWork from "@/views/sections/sectionFive/RecentWork.vue";
import OurTestimonials from "@/views/sections/sectionSix/OurTestimonials.vue";
import Footer from "@/views/sections/sectionSeven/Footer.vue";

import "@/views/Styles/style.css";
import "@/views/Styles/normalise.css";
export default {
  name: "app",
  components: {
    NavBar,
    GetStarted,
    OurBusiness,
    AboutUs,
    RecentWork,
    OurTestimonials,
    Footer
  }
};
</script>
<style>
@import url("https://fonts.googleapis.com/css2?family=Hind+Vadodara:wght@300;400;500;600;700&display=swap");
@import url("https: ; //fonts.googleapis.com/css2?family=Hind+Vadodara:wght@300;400;500;600;700&family=Playfair+Display:wght@700&display=swap");
@import url("https://cdn.jsdelivr.net/npm/swiper@8/swiper-bundle.min.css");
</style>
