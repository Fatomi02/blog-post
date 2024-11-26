<template>
  <div class="flex gap-8 xl:gap-[64px] flex-col xl:px-[32px]">
    <div class="flex flex-col gap-8">
      <h2 class="font-semibold text-[24px] text-[#101828]">All blog posts</h2>
      <div class="grid grid-cols-1 md:grid-cols-2 xl:grid-cols-3 gap-8 w-full">
        <div v-for="(post, index) in allPost" class="flex flex-col gap-8" :key="index">
          <img class="w-full h-[200px] md:h-[240px]" :src="post.image" alt="ui-ux-presentation" />
          <div class="flex flex-col gap-6">
            <div class="flex flex-col gap-3">
              <small class="font-semibold text-[#6941C6]">{{
                post.author
              }} • {{ post.date }}</small>
              <div class="flex justify-between items-center">
                <h2 class="text-[#101828] font-semibold text-xl xl:text-2xl">
                  {{ post.heading }}
                </h2>
                <img src="../assets/icons/wrap-icon.svg" alt="wrap-icon" />
              </div>
              <p class="text-[#667085]">{{ post.description }}</p>
            </div>
            <div class="flex items-center gap-2">
              <button v-for="(tag, index) in post.tags" class="text-[14px] font-medium rounded-2xl py-[2px] px-[10px]"
                :class="[
                  {
                    'bg-[#F9F5FF] text-[#6941C6]':
                      tag === 'Design' || tag === 'Podcasts',
                  },
                  { 'bg-[#EEF4FF] text-[#3538CD]': tag === 'Research' },
                  {
                    'bg-[#ECFDF3] text-[#027A48]':
                      tag === 'Software Development',
                  },
                  { 'bg-[#F9F5FF] text-[#6941C6]': tag === 'Leadership' },
                  { 'bg-[#F0F9FF] text-[#026AA2]': tag === 'Product' },
                  {
                    'bg-[#F8F9FC] text-[#363F72]':
                      tag === 'Management' || tag === 'Customer Success',
                  },
                  { 'bg-[#FFF6ED] text-[#C4320A]': tag === 'Frameworks' },
                  { 'bg-[#FDF2FA] text-[#C11574]': tag === 'Tools' },
                  { 'bg-[#FFF1F3] text-[#C01048]': tag === 'SaaS' },
                ]" :key="index">
                {{ tag }}
              </button>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="border-[#EAECF0] border-t-[1px] py-3 px-4 md:px-0 md:py-0 md:pt-5 flex justify-between items-center">
      <div @click="previous" class="flex gap-2 text-[#667085] text-[14px] items-center font-medium cursor-pointer">
        <img src="../assets/icons/arrow-left.svg" alt="back" />
        <small class="hidden md:block">Previous</small>
      </div>
      <div class="hidden md:flex gap-[2px]">
        <div :class="[
          'rounded-[8px]',
          'w-10',
          'h-10',
          'flex',
          'justify-center',
          'items-center',
          'text-sm',
          'text-[#7F56D9]',
          { 'bg-[#F9F5FF]': count === 1 },
        ]">
          1
        </div>
        <div :class="[
          'rounded-[8px]',
          'w-10',
          'h-10',
          'flex',
          'justify-center',
          'items-center',
          'text-sm',
          'text-[#7F56D9]',
          { 'bg-[#F9F5FF]': count === 2 },
        ]">
          2
        </div>
        <div :class="[
          'rounded-[8px]',
          'w-10',
          'h-10',
          'flex',
          'justify-center',
          'items-center',
          'text-sm',
          'text-[#7F56D9]',
          { 'bg-[#F9F5FF]': count === 3 },
        ]">
          3
        </div>
        <div :class="[
          'rounded-[8px]',
          'w-10',
          'h-10',
          'flex',
          'justify-center',
          'items-center',
          'text-sm',
          'text-[#7F56D9]',
          {
            'bg-[#F9F5FF]':
              count === 4 || count === 5 || count === 6 || count === 7,
          },
        ]">
          ...
        </div>
        <div :class="[
          'rounded-[8px]',
          'w-10',
          'h-10',
          'flex',
          'justify-center',
          'items-center',
          'text-sm',
          'text-[#7F56D9]',
          { 'bg-[#F9F5FF]': count === 8 },
        ]">
          8
        </div>
        <div :class="[
          'rounded-[8px]',
          'w-10',
          'h-10',
          'flex',
          'justify-center',
          'items-center',
          'text-sm',
          'text-[#7F56D9]',
          { 'bg-[#F9F5FF]': count === 9 },
        ]">
          9
        </div>
        <div :class="[
          'rounded-[8px]',
          'w-10',
          'h-10',
          'flex',
          'justify-center',
          'items-center',
          'text-sm',
          'text-[#7F56D9]',
          { 'bg-[#F9F5FF]': count === 10 },
        ]">
          10
        </div>
      </div>
      <div class="font-medium md:hidden text-sm text-[#344054]">
        Page {{ count }} of 10
      </div>
      <div @click="next" class="flex gap-2 text-[#667085] text-[14px] font-medium items-center cursor-pointer">
        <small class="hidden md:block">Next</small>
        <img src="../assets/icons/arrow-right.svg" alt="next" />
      </div>
    </div>
  </div>
</template>

<script>
import { ref } from "vue";

export default {
  name: "AllPost",
  setup() {
    const allPost = [
      {
        image: require("@/assets/images/bill-walsh.png"),
        author: "Alec Whitten",
        date: "17 Jan 2022",
        heading: "Bill Walsh leadership lessons",
        description:
          "Like to know the secrets of transforming a 2-14 team into a 3x Super Bowl winning Dynasty?",
        tags: ["Leadership", "Management"],
      },
      {
        image: require("@/assets/images/pm.png"),
        author: "Demi WIlkinson",
        date: "16 Jan 2022",
        heading: "PM mental models",
        description:
          "Mental models are simple expressions of complex processes or relationships.",
        tags: ["Product", "Research", "Frameworks"],
      },
      {
        image: require("@/assets/images/wireframing.png"),
        author: "Candice Wu",
        date: "15 Jan 2022",
        heading: "What is Wireframing?",
        description:
          "Introduction to Wireframing and its Principles. Learn from the best in the industry.",
        tags: ["Design", "Research"],
      },
      {
        image: require("@/assets/images/collaboration.png"),
        author: "Natali Craig",
        date: "14 Jan 2022",
        heading: "How collaboration makes us better designers",
        description:
          "Collaboration can make our teams stronger, and our individual designs better.",
        tags: ["Design", "Research"],
      },
      {
        image: require("@/assets/images/frameworks.png"),
        author: "Drew Cano",
        date: "13 Jan 2022",
        heading: "Our top 10 Javascript frameworks to use",
        description:
          "JavaScript frameworks make development easy with extensive features and functionalities.",
        tags: ["Software Development", "Tools", "SaaS"],
      },
      {
        image: require("@/assets/images/podcast.png"),
        author: "Orlando Diggs",
        date: "12 Jan 2022",
        heading: "Podcast: Creating a better CX Community",
        description:
          "Starting a community doesn’t need to be complicated, but how do you get started?",
        tags: ["Podcasts", "Customer Success"],
      },
    ];
    let count = ref(1);

    const previous = () => {
      if (count.value === 1) {
        return;
      } else {
        count.value--;
      }
    };

    const next = () => {
      if (count.value === 10) {
        return
      }
      else {
        count.value++;
      }
    };

    return {
      allPost,
      count,
      previous,
      next,
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
