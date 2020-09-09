<template>
  <div>
    <div id="featuredWork" class="pb-6 md:pb-20">
      <div class="mt-8 text-4xl md:text-6xl font-bold md:mt-16 text-center">Featured Work</div>
      <div v-bind:key="index" v-for="(work, index) in worksInput">
        <work
          v-bind:work="work"
          :index="index"
          class="flex flex-col justify-center items-center mt-8 md:mt-32"
          :class="(index % 2 !== 0) ? 'md:flex-row-reverse': 'md:flex-row'"
          @show-slides="showslides(work)"
        />
      </div>
    </div>
  </div>
</template>

<script>
import Work from "./Work.vue";

export default {
  data() {
    return {
      isShowingSlides: false,
    };
  },
  name: "FeaturedWork",
  components: {
    Work
  },
  props: ["worksInput"],
  methods: {
    showslides(work) {
      if (this.isShowingSlides === false) {
        this.isShowingSlides = true;
      } else {
        this.isShowingSlides = false;
      }
      console.log(work);
    },
  },
};
</script>

<style scoped>
@media (min-width: 768px) {
  .m-size-550 {
    height: 550px;
    width: 550px;
  }
}
</style>

