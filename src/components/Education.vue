<template>
  <div id="education" class="pb-20" style="background-color: rgba(255, 165, 0, 0.24);">
    <div class="mt-8 text-4xl md:text-6xl font-bold md:mt-16 text-center pt-12">Education</div>
    <div class="flex justify-center mt-12">
      <div
        v-bind:key="index"
        v-for="(education, index) in education"
        class="p-6"
        style="background-color: #e2e8f0; text-align: center; border: 3px solid black;"
      >
        <div class="font-bold text-xl">{{education.degree}}</div>
        <div class="border-2 rounded-lg mt-3" style="border-color: #ed8936;"></div>
        <div class="mt-3 text-4xl font-bold" style="color: #052371;">{{education.fieldOfStudy}}</div>
        <div class="mt-3">{{education.institution}}</div>
        <div>{{education.years}}</div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Education",
  components: {},
  props: ["education"]
};
</script>

<style>
@media (min-width: 768px) {
  .md-border-8 {
    border-width: 3px;
  }
}
</style>
