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
  <div class="pb-[64px] lg:pb-[96px]">
    <div class="flex flex-col gap-8 xl:px-[32px]">
      <h2 class="font-semibold text-[24px] text-[#101828]">
        Recent blog posts
      </h2>
      <div class="flex flex-col xl:flex-row gap-12 justify-between">
        <div class="flex flex-col gap-8 xl:w-[48%]">
          <img class="w-full h-[200px] md:h-[228px]" src="../assets/images/ui-ux-presentation.png" alt="ui-ux-presentation" />
          <div class="flex flex-col gap-6">
            <div class="flex flex-col gap-3">
              <small class="font-semibold text-[#6941C6]">Olivia Rhye • 20 Jan 2022</small>
              <div class="flex justify-between items-center">
                <h2 class="text-[#101828] font-semibold text-xl xl:text-2xl">
                  UX review presentations
                </h2>
                <img src="../assets/icons/wrap-icon.png" alt="wrap-icon" />
              </div>
              <p class="text-[#667085]">
                How do you create compelling presentations that wow your
                colleagues and impress your managers?
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
        <div class="flex flex-col gap-12 md:flex-row xl:flex-col xl:gap-8 xl:w-[48%]">
          <div class="flex flex-col xl:flex-row gap-6">
            <img class="xl:w-[48%] h-[200px]" src="../assets/images/migrating.png" alt="" />
            <div class="flex flex-col gap-6">
              <div class="flex flex-col gap-3">
                <small class="font-semibold text-[#6941C6]">Phoenix Baker • 19 Jan 2022</small>
                <div class="flex items-center justify-between">
                  <h2 class="text-[#101828] font-semibold text-xl xl:text-2xl">
                    Migrating to Linear 101
                  </h2>
                  <img class="md:hidden" src="../assets/icons/wrap-icon.png" alt="wrap-icon" />
                </div>
                <p class="text-[#667085]">
                  Linear helps streamline software projects, sprints, tasks, and
                  bug tracking. Here’s how to get...
                </p>
              </div>
              <div class="flex items-center gap-2">
                <button class="bg-[#F9F5FF] text-[#6941C6] text-[14px] font-medium rounded-2xl py-[2px] px-[10px]">
                  Design
                </button>
                <button class="bg-[#FDF2FA] text-[#C11574] rounded-2xl text-[14px] font-medium py-[2px] px-[10px]">
                  Research
                </button>
                <button class="bg-[#FFF1F3] text-[#C01048] rounded-2xl text-[14px] font-medium py-[2px] px-[10px] xl:hidden">
                  Presentation
                </button>
              </div>
            </div>
          </div>
          <div class="flex flex-col xl:flex-row gap-6">
            <img class="xl:w-[48%] h-[200px]" src="../assets/images/building.png" alt="" />
            <div class="flex flex-col gap-6">
              <div class="flex flex-col gap-3">
                <small class="font-semibold text-[#6941C6]">Lana Steiner • 18 Jan 2022</small>
                <div class="flex items-center justify-between">
                  <h2 class="text-[#101828] font-semibold text-xl xl:text-2xl">
                    Building your API Stack
                  </h2>
                  <img class="md:hidden" src="../assets/icons/wrap-icon.png" alt="wrap-icon" />
                </div>
                <p class="text-[#667085]">
                  The rise of RESTful APIs has been met by a rise in tools for
                  creating, testing, and manag...
                </p>
              </div>
              <div class="flex items-center gap-2">
                <button class="bg-[#ECFDF3] text-[#027A48] text-[14px] font-medium rounded-2xl py-[2px] px-[10px]">
                  Design
                </button>
                <button class="bg-[#FDF2FA] text-[#C11574] rounded-2xl text-[14px] font-medium py-[2px] px-[10px]">
                  Research
                </button>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
  <div class="flex gap-8 xl:gap-[64px] flex-col xl:px-[32px]">
    <div class="flex flex-col gap-8">
      <h2 class="font-semibold text-[24px] text-[#101828]">All blog posts</h2>
      <div class="grid grid-cols-1 md:grid-cols-2 xl:grid-cols-3 gap-12 w-full">
        <div v-for="(post, index) in allPost" class="flex flex-col gap-8" :key="index">
          <img class="w-full h-[200px] md:h-[240px]" :src="post.image" alt="ui-ux-presentation" />
          <div class="flex flex-col gap-6">
            <div class="flex flex-col gap-3">
              <small class="font-semibold text-[#6941C6]">{{
                post.subHeading
                }}</small>
              <div class="flex justify-between items-center">
                <h2 class="text-[#101828] font-semibold text-xl xl:text-2xl">
                  {{ post.heading }}
                </h2>
                <img src="../assets/icons/wrap-icon.png" alt="wrap-icon" />
              </div>
              <p class="text-[#667085]">{{ post.description }}</p>
            </div>
            <div class="flex items-center gap-2">
              <button v-for="(tag, index) in post.tags" :class="[
                'text-[14px]',
                'font-medium',
                'rounded-2xl',
                'py-[2px]',
                'px-[10px]',
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
        <img src="../assets/icons/arrow-left.png" alt="back" />
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
        <img src="../assets/icons/arrow-right.png" alt="next" />
      </div>
    </div>
  </div>
</template>

<script>
import { ref } from "vue";

export default {
  name: "HomePage",
  setup() {
    const email = ref("");
    const allPost = ref([
      {
        image: require("@/assets/images/bill-walsh.png"),
        subHeading: "Alec Whitten • 17 Jan 2022",
        heading: "Bill Walsh leadership lessons",
        description:
          "Like to know the secrets of transforming a 2-14 team into a 3x Super Bowl winning Dynasty?",
        tags: ["Leadership", "Management"],
      },
      {
        image: require("@/assets/images/pm.png"),
        subHeading: "Demi WIlkinson • 16 Jan 2022",
        heading: "PM mental models",
        description:
          "Mental models are simple expressions of complex processes or relationships.",
        tags: ["Product", "Research", "Frameworks"],
      },
      {
        image: require("@/assets/images/wireframing.png"),
        subHeading: "Candice Wu • 15 Jan 2022",
        heading: "What is Wireframing?",
        description:
          "Introduction to Wireframing and its Principles. Learn from the best in the industry.",
        tags: ["Design", "Research"],
      },
      {
        image: require("@/assets/images/collaboration.png"),
        subHeading: "Natali Craig • 14 Jan 2022",
        heading: "How collaboration makes us better designers",
        description:
          "Collaboration can make our teams stronger, and our individual designs better.",
        tags: ["Design", "Research"],
      },
      {
        image: require("@/assets/images/frameworks.png"),
        subHeading: "Drew Cano • 13 Jan 2022",
        heading: "Our top 10 Javascript frameworks to use",
        description:
          "JavaScript frameworks make development easy with extensive features and functionalities.",
        tags: ["Software Development", "Tools", "SaaS"],
      },
      {
        image: require("@/assets/images/podcast.png"),
        subHeading: "Orlando Diggs • 12 Jan 2022",
        heading: "Podcast: Creating a better CX Community",
        description:
          "Starting a community doesn’t need to be complicated, but how do you get started?",
        tags: ["Podcasts", "Customer Success"],
      },
    ]);
    let count = ref(1);

    const logValue = () => {
      console.log(email.value);
    };

    const previous = () => {
      if (count.value === 1) {
        return;
      } else {
        count.value--;
      }
    };

    const next = () => {
      if(count.value === 10) {
        return
      } 
      else {
        count.value++;
      }
    };

    return {
      email,
      logValue,
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
