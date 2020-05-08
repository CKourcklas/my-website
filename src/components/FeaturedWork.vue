<template>
  <div id="featuredWork" class="pb-20">
    <div class="text-4xl md:text-6xl font-bold mt-16 text-center">Featured Work</div>
    <div v-bind:key="work.id" v-for="work in works">
      <Work
        v-bind:work="work"
        class="flex flex-col md:flex-row justify-center items-center mt-8 md:mt-24"
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

