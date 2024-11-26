<template>
  <div class="w-[88%] xl:w-[1280] mx-auto py-[64px] lg:py-[96px]">
    <BlogHeader />
    <ReactBlog :recentPostData=recentPostData />
    <AllPost />
  </div>
</template>

<script>
import BlogHeader from './components/Header.vue';
import ReactBlog from './components/RecentBlog.vue'
import AllPost from './components/AllPost.vue'

export default {
  name: 'App',
  components: {
    AllPost,
    BlogHeader,
    ReactBlog
  },

  setup() {
    const recentPostData = {
      bigCover: {
        image: require("@/assets/images/ui-ux-presentation.png"),
        author: "Olivia Rhye",
        date: "20 Jan 2022",
        heading: "UX review presentations",
        description:
          "How do you create compelling presentations that wow your colleagues and impress your managers?",
        tags: ["Design", "Research", "Presentation"],
      },
      smallCover: [
      {
        image: require("@/assets/images/migrating.png"),
        author: "Phoenix Baker",
        date: "19 Jan 2022",
        heading: "Migrating to Linear 101",
        description:
          "Linear helps streamline software projects, sprints, tasks, and bug tracking. Here’s how to get...",
        tags: [
          {
            bgColor: "bg-[#F0F9FF]",
            color: "text-[#026AA2]",
            name: "Design"
          },
          {
            bgColor: "bg-[#FDF2FA]",
            color: "text-[#C11574]",
            name: "Research"
          },
        ],
      },
      {
        image: require("@/assets/images/building.png"),
        author: "Lana Steiner",
        date: "18 Jan 2022",
        heading: "Building your API Stack",
        description:
          "The rise of RESTful APIs has been met by a rise in tools for creating, testing, and manag...",
        tags: [          {
            bgColor: "bg-[#ECFDF3]",
            color: "text-[#027A48]",
            name: "Design"
          },
          {
            bgColor: "bg-[#FDF2FA]",
            color: "text-[#C11574]",
            name: "Research"
          },],
      },
      ]
    }

    return {
      recentPostData  
  }
  }

}
</script>

<style>

</style>
