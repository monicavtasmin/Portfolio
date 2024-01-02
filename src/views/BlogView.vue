<template>
  <div class="container mx-auto p-3 md:p-8">
    <div class="flex flex-col-reverse md:flex-row relative">
      <div class="w-full md:w-2/3">
        <div class="flex flex-col gap-4 md:px-20 fade-zoom-up">
          <iframe src="https://docs.google.com/forms/d/e/1FAIpQLSfPAh07hUIBGQ8-mcnW9kz4rzS5dDeBEANyRbzSuAyC1JxVFw/viewform?embedded=true" width="700" height="912" frameborder="0" marginheight="0" marginwidth="0">Loading…</iframe> -->
        </div>
      </div>
      <!-- <div class="w-full md:w-1/3 h-fit p-8 md:sticky md:top-24">
        <div class="flex flex-col text-left">
          <div class="bg-clip-text bg-gradient-to-r from-slate-100 to-amber-300 text-transparent">Let's share experiences,
            stories, and knowledge together.
          </div>
          <div class="h-[1px] mt-7 mb-7 w-20 bg-amber-200 aos-init aos-animate mr-2"></div>
          <div class="hidden md:block">
            <div class="text-white text-md font-semibold">Topics</div>
            <div class="mt-3 flex flex-wrap gap-1">
              <span
                class="py-2 px-3 rounded-2xl bg-[#1e1e1f] hover:bg-white/20 text-white text-xs cursor-pointer">NodeJS</span>
              <span
                class="py-2 px-3 rounded-2xl bg-[#1e1e1f] hover:bg-white/20 text-white text-xs cursor-pointer">Technology</span>
            </div>
          </div>
        </div>
      </div> -->
    </div>
  </div>
  <ArticleList />
</template>
  
<script>
import ArticleList from '@/components/ArticleList.vue';
import axios from "axios";
export default {
  data() {
    return {
      articles: []
    }
  },
  components: {
    ArticleList
  },
  mounted() {
    this.getArticles();
  },
  methods: {
    async getArticles() {
      axios.get('https://64a38c9cc3b509573b564183.mockapi.io/api/blog/all')
        .then(response => {
          this.articles = response.data;
        })
    },

  }
}

</script>