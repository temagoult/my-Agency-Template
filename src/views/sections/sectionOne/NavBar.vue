<template>
  <div class="myContainer md:mb-[50px] sm:mb-[40px] mb-[40px]">
    <div class="flex items-center justify-between">
      <div class="sm:flex hidden sm:w-[40%]">
        <ul
          class="list-none lg:text-[16px] md:text-[15px] sm:text-[14px] text-[12px] w400 mainColor flex md:gap-3 gap-2 cursor-pointer"
        >
          <li>Home</li>
          <li>About Us</li>
          <li>Services</li>
          <li>Contact Us</li>
        </ul>
      </div>
      <div
        class="titleTemplate mainColor w700 lg:text-[24px] md:text-[22px] sm:text-[18px] text-[15px] w-[30%] sm:text-center cursor-pointer"
      >Dream Agency</div>
      <div
        class="w-[30%] gap-[10%] sm:flex justify-end hidden lg:text-[16px] md:text-[15px] sm:text-[14px] text-[12px]"
      >
        <i
          class="icon fa-brands fa-facebook bg-transparent mainColor lg:w-[10px] lg:h-[20px] md:w-[9px] md:h-[18px] h-[15px] p-1"
        ></i>

        <i
          class="icon fa-brands fa-linkedin-in bg-transparent mainColor lg:w-[10px] lg:h-[20px] md:w-[9px] md:h-[18px] h-[15px] p-1"
        ></i>

        <i
          class="icon fa-brands fa-instagram bg-transparent mainColor lg:w-[10px] lg:h-[20px] md:w-[9px] md:h-[18px] h-[15px] p-1"
        ></i>
      </div>
      <div class="sm:hidden mainColor">
        <div v-if="display">
          <div @click="onDisplay" class="flex items-start h-[20px]">
            <i class="fa-solid fa-xmark text-[14px] cursor-pointer"></i>
          </div>
        </div>

        <div v-else class>
          <div @click="onDisplay" class="flex items-start h-[20px]">
            <i class="fa-solid fa-bars text-[14px] cursor-pointer"></i>
          </div>
        </div>
      </div>
    </div>
    <div :class="this.display?'sm:hidden':'hidden'">
      <ul
        class="list-none lg:text-[16px] md:text-[15px] sm:text-[14px] text-[12px] w400 mainColor flex flex-col md:gap-2 gap-1"
      >
        <li
          class="border border-solid border-x-transparent border-t-transparent border-b-[#331B3B]"
        >Home</li>
        <li
          class="border border-solid border-x-transparent border-t-transparent border-b-[#331B3B]"
        >About Us</li>
        <li
          class="border border-solid border-x-transparent border-t-transparent border-b-[#331B3B]"
        >Services</li>
        <li>Contact Us</li>
      </ul>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      display: false
    };
  },
  name: "navBar",
  methods: {
    onDisplay() {
      this.display = !this.display;
    }
  }
};
</script>