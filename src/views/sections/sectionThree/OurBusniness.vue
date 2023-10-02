<template>
  <div class="business relative md:mb-[100px] sm:mb-[70px] mb-[40px]">
    <div class="z-[99] flex flex-col gap-6 justify-end md:mt-8 sm:mt-8 myContainer">
      <div class="partOne text-center">
        <div
          class="titleSection mainColor lg:text-[48px] md:text-[34px] sm:text-[23px] text-[29px]"
        >
          <span class="w700">What We Do</span>
          <br class />
          <span class="w300">For Your</span>

          <span class="w300 low-highlight p-2">Business</span>
        </div>
      </div>

      <div
        class="parTwo flex sm:flex-row flex-col gap-7 ml-4 sm:items-end items-center sm:overflow-x-visible overflow-x-hidden"
      >
        <div class="nextPrev sm:flex flex gap-3 sm:order-1 order-2">
          <div
            :class=" this.prevActif?'actif nextButt flex items-center justify-center text-[22px] cursor-pointer':'nextButt flex items-center justify-center text-[22px] cursor-pointer'"
            @click="onPrevious"
          >{{ sup }}</div>
          <div
            :class="this.nextActif?'actif previousButt flex items-center justify-center text-[22px]  cursor-pointer':'previousButt flex items-center justify-center text-[22px]  cursor-pointer'"
            @click="onNext"
          >{{ inf }}</div>
        </div>
        <Swiper
          class="w-[120%] sm:order-2 order-1"
          @swiper="getRef"
          ref="mySwiper"
          slidesPerView="auto"
          mousewheel
          freeMode
          loop
          autoplay
        >
          <Swiper-slide
            v-for="(card,index) in cardBusiness"
            :key="index"
            class="sm:w-[350px] w-[100%]"
          >
            <div
              class="businessCard flex flex-col justify-center items-start gap-2 sm:w-[90%] w-[88%] cursor-pointer"
            >
              <img :src="card.image" class="w-[52px] h-[48px] px-2" alt />
              <div class="titreBusiness px-2">{{ card.title }}</div>
              <p class="paraBusiness px-2">{{ card.paragraph }}</p>
            </div>
          </Swiper-slide>
        </Swiper>
      </div>
    </div>
    <img
      src="../../../assets//images/test.png"
      class="absolute sm:w-[90%] w-[130%] sm:h-[110%] h-[100%] top-0 z-[-1]"
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
      cardBusiness: [
        {
          image: require("../../../assets//images/rec1.svg"),
          title: "Website Design",
          paragraph:
            "Lorem Ipsum has been the industry's standard dummy text ever since the 1500s."
        },
        {
          image: require("../../../assets//images/rec2.svg"),
          title: "Website Design",
          paragraph:
            "Lorem Ipsum has been the industry's standard dummy text ever since the 1500s."
        },
        {
          image: require("../../../assets//images/rec3.svg"),
          title: "Mobile APP Development",
          paragraph:
            "Lorem Ipsum has been the industry's standard dummy text ever since the 1500s."
        },
        {
          image: require("../../../assets//images/rec4.svg"),
          title: "Marketing",
          paragraph:
            "Lorem Ipsum has been the industry's standard dummy text ever since the 1500s."
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
  width: 350px;
}
</style>
