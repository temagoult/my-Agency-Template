<template>
  <div
    class="myContainer md:mb-[100px] sm:mb-[70px] mb-[40px] grid sm:grid-cols-2 grid-cols-1 lg:gap-7 md:gap-5 sm:gap-3 gap-2"
  >
    <div class="partOne flex flex-col sm:gap-6 gap-3 justify-center sm:text-start text-center">
      <div
        class="titleSection mainColor lg:text-[87px] md:text-[71px] sm:text-[42px] text-[29px] lg:leading-[85px] md:leading-[80px] sm:leading-[50px]"
      >
        <span class="w700">We Help you</span>
        <br class />
        <span class="w300">to grow your</span>
        <br class />
        <span class="w300 low-highlight p-2">Business</span>
      </div>
      <p class="lg:text-[16px] md:text-[15px] sm:text-[13px] text-[12px] sm:text-start text-center">
        Lorem Ipsum has been the industry's standard dummy text ever
        <br class="sm:block hidden" />since the 1500s, when an unknown printer took a galley of type and
        <br class="sm:block hidden" />scrambled it to make a type specimen book.
      </p>
      <div class="sm:self-start self-center">
        <button
          class="cursor-pointer p-2 lg:text-[17px] md:text-[12px] sm:text-[9px] text-[8px] inputfield bg-[#331B3B] lg:w-[207px] lg:h-[66px] md:w-[144px] md:h-[46px] sm:w-[111px] sm:h-[32px] w-[79px] h-[23px] flex justify-center items-center rounded-[10px]"
        >Get Started</button>
      </div>
    </div>
    <div class="z-[99] sm:h-[auto] sm:w-[109%] relative sm:flex hidden cursor-pointer">
      <img src="../../../assets//images/home.png" class />
    </div>
  </div>
</template> 
<script>
export default {
  data() {
    return {};
  },
  name: "GetStarted"
};
</script>