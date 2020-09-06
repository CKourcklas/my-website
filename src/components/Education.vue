<template>
  <div id="education" class="pb-20 px-4" style="background-color: rgba(237, 137, 54, 0.75)">
    <div class="mt-8 text-4xl md:text-6xl font-bold md:mt-16 text-center pt-12">Education</div>
    <div class="flex flex-col flex-wrap md:flex-row justify-center items-center md:justify-evenly mt-5 md:mt-12">
      <div
        v-bind:key="index"
        v-for="(educationItem, index) in educationItem"
        class="p-6 text-center mt-5 md:mt-0 r-width mb-4"
        style="background-color: #e2e8f0; border: 3px solid black;"
      >
        <div class="font-bold md:text-lg uppercase">{{educationItem.degree}}</div>
        <div class="border-2 rounded-lg mt-3" style="border-color: #ed8936;"></div>
        <div class="mt-3 text-xl md:text-4xl font-bold" style="color: #052371; min-width: 275px;">{{educationItem.fieldOfStudy}}</div>
        <div class="mt-3">{{educationItem.institution}}</div>
        <div>{{educationItem.years}}</div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Education",
  components: {},
  data() {
    return {
      educationItem: [
        {
          degree: "Associate of Applied Business",
          fieldOfStudy: "Programming",
          institution: "Cuyahoga Community College",
          years: "2015-2017"
        },
        {
          degree: "Bachelor of Business Administration",
          fieldOfStudy: "Marketing",
          institution: "The University of Akron",
          years: "2009-2013"
        },

        {
          degree: "Master of Science",
          fieldOfStudy: "Digital Sciences",
          institution: "Kent State University",
          years: "2019-Present"
        }
      ]
    };
  }
};
</script>

<style>
@media (min-width: 768px) {
  .md-border-8 {
    border-width: 3px;
  }
}

@media (min-width: 768px) {
  .r-width{
    width: 450px;
    min-width: 350px;
  }
}
</style>
