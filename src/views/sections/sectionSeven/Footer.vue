
<template>
  <div
    class="md:mb-[100px] sm:mb-[70px] mb-[40px] footer h-[100%] grid sm:grid-cols-2 grid-cols-1 p-12 md:gap-7 sm:gap-5 gap-3"
  >
    <div
      class="partOneFooter flex flex-col justify-evenly gap-3 sm:text-start text-center sm:items-start items-center"
    >
      <div class="logoFooter">Dream Agency</div>
      <p class="text-[#FFF] lg:text-[16px] md:text-[15px] sm:text-[13px] text-[12px]">
        Lorem Ipsum has been the industry's standard dummy text
        <br class="md:block hidden" />ever since the 1500s, when an unknown printer took a galley
        <br class="md:block hidden" />of type and scrambled it to make a type specimen book. It
        <br class="md:block hidden" />has survived not only five centuries.
      </p>
      <div class="getInTouch lg:text-[16px] md:text-[15px] sm:text-[13px] text-[12px]">Get In Touch</div>
      <div class="inputField flex">
        <input
          placeholder="Enter Your Email "
          class="input flex p-1 lg:w-[263px] lg:h-[52px] md:w-[230px] md:h-[45px] sm:w-[200px] sm:h-[40px] w-[150px] h-[30px] placeholder:lg:text-[16px] placeholder:md:text-[15px] placeholder:sm:text-[13px] placeholder:text-[12px]"
        />
        <div
          class="cursor-pointer send flex justify-center items-center md:h-[45px] lg:w-[143px] lg:h-[52px] sm:w-[120px] sm:h-[40px] w-[70px] h-[30px] lg:text-[16px] md:text-[15px] sm:text-[13px] text-[8px]"
        >send</div>
      </div>
    </div>
    <div class="partTwoFooter flex justify-stretch">
      <img
        src="../../../assets//images/photoFooter.png"
        class="partTwoFooterPhoto cursor-pointer"
        alt
      />
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {};
  },
  // eslint-disable-next-line vue/multi-word-component-names
  name: "Footer"
};
</script>