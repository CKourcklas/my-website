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

import StudyBuddyCoverImage from "@/assets/img/StudyBuddy/StudyBuddy1.jpg";
import GTWCoverImage from "@/assets/img/GTW/GTW1.jpg";
import KSUWFCoverImage from "@/assets/img/KSUWF/KSUWF1.jpg";
import ETWCoverImage from "@/assets/img/ETW/ETW1.jpg";
import MMPCoverImage from "@/assets/img/MMP/MMP1.jpg";

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
          image: StudyBuddyCoverImage,
          imageDesc: "Study Buddy Cover",
          skills: ["SQL", "Outsystems", "Responsive", "Javascript"]
        },
        {
          title: "Graduate Assistant Tuition Waiver",
          description:
            "Lorem Ipsum is simply dummy text of the printing and typesetting industry. " +
            "Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a" +
            "galley of type and scrambled it to make a type specimen book.",
          image: GTWCoverImage,
          skills: [
            "Skill One",
            "Skill Two",
            "Skill Three",
            "Skill Four",
            "Skill Five"
          ]
        },
        {
          title: "KSU Workflow Management",
          description:
            "Lorem Ipsum is simply dummy text of the printing and typesetting industry. " +
            "Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a" +
            "galley of type and scrambled it to make a type specimen book.",
          image: KSUWFCoverImage,
          skills: [
            "Skill One",
            "Skill Two",
            "Skill Three",
            "Skill Four",
            "Skill Five"
          ]
        },
        {
          title: "Employee Transaction Workflow",
          description:
            "Lorem Ipsum is simply dummy text of the printing and typesetting industry. " +
            "Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a" +
            "galley of type and scrambled it to make a type specimen book.",
          image: ETWCoverImage,
          skills: ["Skill One", "Skill Two", "Skill Three", "Skill Four"]
        },
        {
          title: "Manage My Program",
          description:
            "Lorem Ipsum is simply dummy text of the printing and typesetting industry. " +
            "Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a" +
            "galley of type and scrambled it to make a type specimen book.",
          image: MMPCoverImage,
          skills: ["Skill One", "Skill Two", "Skill Three", "Skill Four"]
        }
      ]
    };
  }
};
</script>

<style>
</style>
