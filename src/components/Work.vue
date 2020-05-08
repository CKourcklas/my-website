<template>
  <div>
    <div class="h-64 w-64 m-size-550 md:relative md:border-8" style="border-color: #ed8936">
      <img
        v-bind:src="work.image"
        :alt="work.imageDesc"
        class="m-size-550 md:absolute shadow object-cover"
        style="right: 40px; bottom: 25px;"
      />
    </div>
    <div class="md:w-16"></div>
    <div class="pl-4 pr-4 md:p-0 max-w-xl">
      <div class="text-lg md:text-4xl font-bold">{{work.title}}</div>
      <div class="mt-4">{{work.description}}</div>
      <div class="mt-6 md:mt-12 uppercase font-bold md:text-lg">Skills Used</div>
      <div class="flex flex-wrap justify-center md:justify-start mt-4">
        <div
          v-bind:key="skill.index"
          v-for="skill in work.skills"
          class="font-bold text-lg bg-gray-300 rounded-lg mt-5 mr-5 p-4 text-center"
          style="min-width: 6rem;"
        >{{skill}}</div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "work",
  props: ["work"]
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