<template>
  <div class="flex flex-col md:flex-row justify-center items-center mt-8 md:mt-24">
    <div class="h-64 w-64 m-size-550 md:relative md:border-8" style="border-color: #ed8936">
      <img
        v-bind:src="work.image"
        :alt="work.imageDesc"
        class="m-size-550 md:absolute shadow object-cover"
        style="right: 40px; bottom: 25px;"
      />
    </div>
    <div class="md:ml-12 max-w-xl">
      <div class="text-4xl font-bold">{{work.title}}</div>
      <div class="mt-4">{{work.description}}</div>
      <div class="mt-12 uppercase font-bold text-lg">Skills Used</div>
      <div class="flex flex-wrap mt-4">
        <div
          v-bind:key="skill.index"
          v-for="skill in work.skills"
          class="font-bold text-lg bg-gray-300 rounded-lg mt-5 mr-5 p-4"
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