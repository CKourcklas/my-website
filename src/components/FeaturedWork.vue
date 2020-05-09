<template>
  <div id="featuredWork" class="pb-20">
    <div class="mt-8 text-4xl md:text-6xl font-bold md:mt-16 text-center">Featured Work</div>
    <div v-bind:key="index" v-for="(work, index) in works">
      <Work
        v-bind:work="work" :index="index"
        class="flex flex-col justify-center items-center mt-8 md:mt-24"
        :class="(index % 2 !== 0) ? 'md:flex-row-reverse': 'md:flex-row'"
      />
    </div>
  </div>
</template>

<script>
import Work from "./Work.vue";

export default {
  name: "FeaturedWork",
  components: {
    Work
  },
  props: ["works"]
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

