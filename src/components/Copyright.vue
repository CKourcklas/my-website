<template>
  <div id="Copyright" class="px-8 md:px-0 py-10 md:py-24 text-center">
    <div class="font-bold md:font-normal md:text-2xl">
      Built with
      <a href="https://vuejs.org/">Vue.js</a> and
      <a href="https://tailwindcss.com/">Tailwind CSS</a>
    </div>
    <div class="mt-2">&#169; Cory Kourcklas 2020. All rights reserved.</div>
  </div>
</template>

<script>
export default {
  name: "Copyright",
  components: {}
};
</script>

<style scoped>
a:hover {
  color: blue;
  text-decoration: underline;
}
</style>
