<template>
  <div class="business relative md:mb-[100px] sm:mb-[70px] mb-[40px]">
    <div class="z-[99] flex flex-col gap-6 justify-end md:mt-8 sm:mt-8 myContainer">
      <div
        class="partOne sm:text-start text-center flex justify-between items-center sm:flex-row flex-col gap-3"
      >
        <div
          class="titleSection mainColor lg:text-[48px] md:text-[34px] sm:text-[23px] text-[29px]"
        >
          <span class="w700">Our Recent Work</span>
          <br class />
          <span class="w300">By Our</span>

          <span class="w300 low-highlight p-2">Expert</span>
        </div>
        <p class="lg:text-[17px] md:text-[15px] sm:text-[13px] text-[12px]">
          Lorem Ipsum has been the industry's standard dummy text ever
          <br />since the 1500s, when an unknown printer took a galley of type and
          <br />scrambled it to make a type specimen book.
        </p>
      </div>

      <div class="parTwo sm:flex flex flex-col gap-7 ml-4 sm:items-start items-center">
        <Swiper
          class="w-[120%] sm:order-2 order-1 lg:ml-[13%] md:ml-[9%] sm:ml-[8%]"
          @swiper="getRef"
          ref="mySwiper"
          slidesPerView="auto"
          mousewheel
          freeMode
          loop
          autoplay
        >
          <Swiper-slide
            v-for="(card,index) in cardRecentWork"
            :key="index"
            class="sm:w-[440px] w-[120%]"
          >
            <div
              class="recentCard flex flex-col justify-center items-start gap-2 sm:w-[90%] w-[70%] cursor-pointer"
            >
              <div class="flex w-[95%]">
                <img :src="card.image1" class="imgWork1 sm:w-[100%] w-[70%]" alt />
                <img :src="card.image2" class="imgWork2 sm:w-[100%] w-[70%]" alt />
              </div>
              <div class="flex justify-between items-center w-[98%]">
                <div class="recentwordlabel px-2 sm:text-[24px] text-[20px]">{{ card.title }}</div>
                <button class="btnviewwork text-[14px] text-[#331B3B]">View Work</button>
              </div>
            </div>
          </Swiper-slide>
        </Swiper>
        <div class="nextPrev sm:flex flex gap-3 order-2 lg:ml-[5%] md:ml-[3%]">
          <div
            :class=" this.prevActif?'actif nextButt flex items-center justify-center text-[22px] cursor-pointer':'nextButt flex items-center justify-center text-[22px] cursor-pointer'"
            @click="onPrevious"
          >{{ sup }}</div>
          <div
            :class="this.nextActif?'actif previousButt flex items-center justify-center text-[22px]  cursor-pointer':'previousButt flex items-center justify-center text-[22px]  cursor-pointer'"
            @click="onNext"
          >{{ inf }}</div>
        </div>
      </div>
    </div>
    <img
      src="../../../assets//images/text2.png"
      class="absolute sm:w-[100%] w-[130%] sm:h-[105%] h-[100%] top-0 z-[-1] lg:ml-[10%] md:ml-[8%] sm:ml-[4%]"
      alt
    />
  </div>
</template>
  <script>
import { Scrollbar, Mousewheel, Navigation, Autoplay } from "swiper";
import { SwiperCore, Swiper, SwiperSlide } from "swiper-vue2";
import "swiper/swiper-bundle.css";
SwiperCore.use([Scrollbar, Mousewheel, Navigation, Autoplay]);
export default {
  data() {
    return {
      swiper: null,
      nextActif: false,
      prevActif: false,
      sup: "<",
      inf: ">",
      cardRecentWork: [
        {
          image1: require("../../../assets//images/Mask Group.svg"),
          image2: require("../../../assets//images/Mask Group (1).svg"),
          title: "UI Soup"
        },
        {
          image1: require("../../../assets//images/Mask Group2 .svg"),
          image2: require("../../../assets//images/Mask Group2 (1).svg"),
          title: "Goldcrown Labs"
        },
        {
          image1: require("../../../assets//images/Mask Group.svg"),
          image2: require("../../../assets//images/Mask Group (1).svg"),
          title: " Close Concierge"
        }
      ],
      swiperOptions: {
        slidesPerView: "auto",
        spaceBetween: 0,
        freeMode: true,
        scrollbar: true,
        mousewheel: true,
        breakpoints: {
          640: {
            slidesPerView: 2,
            spaceBetween: 8,
            pagination: {
              el: ".swiper-pagination",
              type: "bullets"
            }
          }
        }
      }
    };
  },
  name: "OurBusiness",
  methods: {
    getRef(swiper) {
      this.swiper = swiper;
    },

    onNext() {
      this.swiper.slideNext();
      this.nextActif = true;
      this.prevActif = false;
    },
    onPrevious() {
      this.swiper.slidePrev();
      this.nextActif = false;
      this.prevActif = true;
    }
  },
  components: {
    Swiper,
    SwiperSlide
  }
};
</script>
  <style scoped>
.swiper-slide {
  display: flex;
  justify-content: center;
  flex-direction: column;
  width: 435px;
}
</style>
  