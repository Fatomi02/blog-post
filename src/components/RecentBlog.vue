<template>
    <div class="pb-[64px] lg:pb-[96px]">
        <div class="flex flex-col gap-8 xl:px-[32px]">
          <h2 class="font-semibold text-[24px] text-[#101828]">
            Recent blog posts
          </h2>
          <div class="flex flex-col xl:flex-row gap-8">
            <div class="flex flex-col gap-8 xl:w-full">
              <img class="w-full h-[200px] md:h-[228px]" :src=recentPostData.bigCover.image alt="ui-ux-presentation" />
              <div class="flex flex-col gap-6">
                <div class="flex flex-col gap-3">
                  <small class="font-semibold text-[#6941C6]"> {{ recentPostData.bigCover.author }} • {{ recentPostData.bigCover.date }} </small>
                  <div class="flex justify-between items-center">
                    <h2 class="text-[#101828] font-semibold text-xl xl:text-2xl">
                      {{ recentPostData.bigCover.heading }}
                    </h2>
                    <img src="../assets/icons/wrap-icon.svg" alt="wrap-icon" />
                  </div>
                  <p class="text-[#667085]">
                    {{ recentPostData.bigCover.description }}
                  </p>
                </div>
                <div class="flex items-center gap-2">
                  <button class="bg-[#F9F5FF] text-[#6941C6] text-[14px] font-medium rounded-2xl py-[2px] px-[10px]">
                    Design
                  </button>
                  <button class="bg-[#EEF4FF] rounded-2xl text-[#3538CD] text-[14px] font-medium py-[2px] px-[10px]">
                    Research
                  </button>
                  <button class="bg-[#FDF2FA] text-[#C11574] rounded-2xl text-[14px] font-medium py-[2px] px-[10px]">
                    Presentation
                  </button>
                </div>
              </div>
            </div>
            <div class="flex flex-col gap-12 md:flex-row xl:flex-col xl:gap-8 xl:w-full">
              <div v-for="(post, index) in recentPostData.smallCover" :key="index" class="flex flex-col xl:flex-row gap-6">
                <img class="xl:w-[320px] h-[200px]" :src=post.image alt="" />
                <div class="flex flex-col gap-6">
                  <div class="flex flex-col gap-3">
                    <small class="font-semibold text-[#6941C6]"> {{ post.author }} • {{ post.date }}</small>
                    <div class="flex items-center justify-between">
                      <h2 class="text-[#101828] font-semibold text-xl xl:text-[18px]">
                        {{ post.heading }}
                      </h2>
                      <img class="md:hidden" src="../assets/icons/wrap-icon.svg" alt="wrap-icon" />
                    </div>
                    <p class="text-[#667085] text-[15.7px]">
                      {{ post.description }}
                    </p>
                  </div>
                  <div class="flex items-center gap-2">
                    <button v-for="(tag, index) in post.tags" :key="index" :class="[tag.bgColor, tag.color]" class="text-[14px] font-medium rounded-2xl py-[2px] px-[10px]">
                        {{ tag.name }}
                    </button>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
  </template>
  
  <script>
  
  export default {
    name: "ReactBlog",
    props: {
      recentPostData: {
      type: Object,
      required: true, // Ensure the parent must provide this prop
    },
    },
    setup() {

      return {
      };
    },
  };
  </script>
  