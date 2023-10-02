<template>
  <div
    class="business myContainer sm:text-start text-center relative md:mb-[100px] sm:mb-[70px] mb-[40px] myContainer grid sm:grid-cols-2 grid-cols-1 lg:gap-9 md:gap- sm:gap-3 gap-2"
  >
    <div class="partOne1">
      <img src="../../../assets//images/aboutus.png" class="md:w-[580px] cursor-pointer" alt />
    </div>
    <div class="parttwo flex flex-col sm:gap-6 gap-3 justify-center sm:text-start text-center">
      <div class="titleSection mainColor lg:text-[48px] md:text-[34px] sm:text-[23px] text-[29px]">
        <span class="w700">About Us</span>
        <br class />
        <span class="w300">Fake Or</span>
        <span class="w300 low-highlight p-2">Real</span>
      </div>
      <p class="lg:text-[17px] md:text-[15px] sm:text-[13px] text-[12px]">
        Lorem Ipsum has been the industry's standard dummy text ever
        <br class="sm:block hidden" />since the 1500s, when an unknown printer took a galley of type and
        <br class="sm:block hidden" />scrambled it to make a type specimen book.
      </p>
      <p class="lg:text-[17px] md:text-[15px] sm:text-[13px] text-[12px]">
        Lorem Ipsum has been the industry's standard dummy text ever
        <br class="sm:block hidden" />since the 1500s, when an unknown printer took a galley of type and
        <br class="sm:block hidden" />scrambled it to make a type specimen book.
      </p>
      <div class="sm:self-start self-center">
        <button
          class="cursor-pointer p-2 lg:text-[17px] md:text-[12px] sm:text-[9px] text-[8px] inputfield bg-[#331B3B] lg:w-[207px] lg:h-[66px] md:w-[144px] md:h-[46px] sm:w-[111px] sm:h-[32px] w-[79px] h-[23px] flex justify-center items-center rounded-[10px]"
        >Explore More</button>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {};
  },
  name: "AboutUs"
};
</script>