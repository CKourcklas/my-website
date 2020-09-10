<template>
  <div id="app">
    <intro />
    <featured-work v-bind:worksInput="worksArray" />
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
    Copyright,
  },
  data() {
    return {
      worksArray: [
        {
          title: "Study Buddy",
          description:
            "Study Buddy is a student-facing flashcard application managed by professors, where analytical data of student study habits is gathered, allowing for " +
            "better curation of course material geared toward student success.",
          imageDesc: "Study Buddy Cover",
          skills: ["SQL", "Outsystems", "Responsive", "Javascript"],
          slides: [
            require("../src/assets/img/StudyBuddy/StudyBuddy1.jpg"),
            require("../src/assets/img/StudyBuddy/StudyBuddy2.jpg"),
            require("../src/assets/img/StudyBuddy/StudyBuddy3.jpg"),
            require("../src/assets/img/StudyBuddy/StudyBuddy4.jpg"),
          ],
          slidesLength: 3,
        },
        {
          title: "Graduate Assistant Tuition Waiver",
          description:
            "Graduate Assistant Tuition Waiver is a digital replacement for over a decade old paper process where administrators can manage the creation and approval of tuition " +
            "waivers for graduate students in real time using Business Process Technology.",
          skills: [
            "BPT (Workflow)",
            "Business Systems Analysis",
            "CI/CD",
            "Outsystems",
          ],
          slides: [
            require("../src/assets/img/GTW/GTW1.jpg"),
            require("../src/assets/img/GTW/GTW2.jpg"),
            require("../src/assets/img/GTW/GTW3.jpg"),
            require("../src/assets/img/GTW/GTW4.jpg"),
          ],
          slidesLength: 3,
        },
        {
          title: "KSU Workflow Management",
          description:
            "KSU Workflow Management is a complete workflow management tool that allows for tracking of submissions across all applications, configuration of workflow " +
            "steps, management of approval chains, proxy assignment, and more.",
          skills: [
            "BPT (Workflow)",
            "SQL",
            "Outsystems",
            "Component-Based Development",
          ],
          slides: [
            require("../src/assets/img/KSUWF/KSUWF1.jpg"),
            require("../src/assets/img/KSUWF/KSUWF2.jpg"),
            require("../src/assets/img/KSUWF/KSUWF3.jpg"),
            require("../src/assets/img/KSUWF/KSUWF4.jpg"),
          ],
          slidesLength: 3,
        },
        {
          title: "PayOnline",
          description:
            "PayOnline is the online payment system for Kent State University. It is utilized by students, authorized parents/guardians of students, and vendors. If a bill is paid " +
            "online at KSU, PayOnline is the system that is used.",
          skills: ["ASP.NET Web", "C#", "Responsive", "SSMS"],
          slides: [
            require("../src/assets/img/PayOnline/PayOnline1.jpg"),
            require("../src/assets/img/PayOnline/PayOnline2.jpg"),
            require("../src/assets/img/PayOnline/PayOnline3.jpg"),
          ],
          slidesLength: 2,
        },
        {
          title: "Manage My Program",
          description:
            "Manage My Program is the application students use to manage Majors, Minors, and Certificates at Kent State University. Students can see approved changes " +
            "to their program in real-time. To date, over 30,000 " +
            "students have made changes to their program using MMP.",
          skills: [
            "SQL",
            "Outsystems",
            "BPT (Workflow)",
            "CI/CD",
            "Business Systems Analysis",
          ],
          slides: [
            require("../src/assets/img/MMP/MMP1.jpg"),
            require("../src/assets/img/MMP/MMP2.jpg"),
            require("../src/assets/img/MMP/MMP3.jpg"),
            require("../src/assets/img/MMP/MMP4.jpg"),
          ],
          slidesLength: 3,
        },
      ],
    };
  },
};
</script>

<style>
</style>
