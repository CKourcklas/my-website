<template>
  <div id="app">
    <intro />
    <featured-work v-bind:works="works" />
    <education />
    <contact />
    <copyright />
  </div>
</template>

<script>
import Intro from "./components/Intro.vue";
import FeaturedWork from "./components/FeaturedWork.vue";
import Education from "./components/Education.vue";
import Contact from "./components/Contact.vue";
import Copyright from "./components/Copyright.vue";

export default {
  name: "App",
  components: {
    Intro,
    FeaturedWork,
    Education,
    Contact,
    Copyright
  },
  data() {
    return {
      works: [
        {
          title: "Study Buddy",
          description:
            "Lorem Ipsum is simply dummy text of the printing and typesetting industry. " +
            "Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a" +
            "galley of type and scrambled it to make a type specimen book.",
          image: require('@/assets/img/StudyBuddy/StudyBuddy1.jpg'),
          imageDesc: "Study Buddy Cover",
          skills: ["SQL", "Outsystems", "Responsive", "Javascript"]
        },
        {
          title: "Graduate Assistant Tuition Waiver",
          description:
            "Lorem Ipsum is simply dummy text of the printing and typesetting industry. " +
            "Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a" +
            "galley of type and scrambled it to make a type specimen book.",
          imageUrl: "",
          skills: ["Skill One", "Skill Two", "Skill Three", "Skill Four"]
        },
        {
          title: "KSU Workflow Management",
          description:
            "Lorem Ipsum is simply dummy text of the printing and typesetting industry. " +
            "Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a" +
            "galley of type and scrambled it to make a type specimen book.",
          imageUrl: "",
          skills: ["Skill One", "Skill Two", "Skill Three", "Skill Four"]
        }
      ]
    };
  }
};
</script>

<style>
</style>
