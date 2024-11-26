<template>
    <div class="w-full flex flex-col gap-8 lg:gap-10 items-center text-center pb-[64px] lg:pb-[96px]">
      <div class="flex flex-col gap-4 lg:gap-6">
        <div class="flex flex-col gap-3">
          <p class="text-[#7F56D9] font-semibold">Our blog</p>
          <h1 class="text-[36px] leading-[44px] lg:text-[48px] font-semibold text-[#101828]">
            Stories and interviews
          </h1>
        </div>
        <p class="text-[#667085] text-[18px] lg:text-xl w-full lg:w-[768px] text-center">
          Subscribe to learn about new product features, the latest in technology,
          solutions, and updates.
        </p>
      </div>
      <div class="flex flex-col w-full justify-center lg:flex-row items-start gap-4">
        <div class="text-start w-full lg:w-[360px] flex flex-col gap-2">
          <input class="border w-full border-[#D0D5DD] py-3 pl-4 pr-[14px] rounded-lg" type="text" @input="logValue"
            v-model="email" placeholder="Enter your email" />
          <p class="text-sm text-[#667085]">
            We care about your data in our <a class="underline leading-5" href="/">privacy policy</a>
          </p>
        </div>
        <button class="py-3 px-5 lg:w-[118px] bg-[#7F56D9] rounded-lg border border-[#7F56D9] btn-shadow w-full">
          Subscribe
        </button>
      </div>
    </div>
  </template>
  
  <script>
  import { ref } from "vue";
  
  export default {
    name: "BlogHeader",
    setup() {
      const email = ref("");

      const logValue = () => {
        console.log(email.value);
      };
      return {
        email,
        logValue,
      };
    },
  };
  </script>
  
  <style>
  .btn-shadow {
    box-shadow: 0px 1px 2px 0px #1018280d;
    color: #fff;
    font-weight: 500;
  }
  </style>
  