<template>
  <div
    class="md:mb-[100px] sm:mb-[70px] mb-[40px] flex flex-col items-center md:gap-9 sm:gap-7 gap-3 myContainer"
  >
    <div class="partOne">
      <div
        class="titleSection mainColor lg:text-[48px] md:text-[34px] sm:text-[23px] text-[29px] text-center"
      >
        <span class="w700">Our Testimonials</span>
        <br class />
        <span class="w300">What Our Clients Are</span>

        <span class="w300 low-highlight p-2">Saying</span>
      </div>
    </div>
    <div class="partTwo flex md:flex-row flex-col gap-8">
      <div
        class="boxClient mx-3 p-4 flex flex-col justify-evenly sm:w-[448px] w-[300px] sm:h-[310px] h-[200px]"
        v-for="(avisClient,index) in avisClients"
        :key="index"
      >
        <img
          src="../../../assets//images/virgule.svg"
          class="md:w-[64px] md:h-[64px] sm:w-[44px] sm:h-[35px] w-[64px] h-[35px]"
          alt
        />
        <p class="lg:text-[16px] md:text-[15px] sm:text-[13px] text-[12px]">{{ avisClient.avis }}</p>
        <div class="label flex gap-1 items-center">
          <div class="tag"></div>
          <div
            class="label lg:text-[16px] md:text-[15px] sm:text-[13px] text-[12px] cursor-pointer"
          >UI Soup</div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      avisClients: [
        {
          clientName: "",
          avis:
            "Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries."
        },
        {
          clientName: "",
          avis:
            "Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries."
        }
      ]
    };
  }
};
</script>