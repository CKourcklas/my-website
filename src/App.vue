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
import PayOnlineCoverImage from "@/assets/img/PayOnline/PayOnline1.jpg";
import MMPCoverImage from "@/assets/img/MMP/MMP1.jpg";

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
      works: [
        {
          title: "Study Buddy",
          description:
            "Study Buddy is a student-facing flashcard application managed by professors, where analytical data of student study habits is gathered, allowing for " +
            "better curation of course material geared toward student success.",
          image: StudyBuddyCoverImage,
          imageDesc: "Study Buddy Cover",
          skills: ["SQL", "Outsystems", "Responsive", "Javascript"],
        },
        {
          title: "Graduate Assistant Tuition Waiver",
          description:
            "Graduate Assistant Tuition Waiver is a digital replacement for over a decade old paper process where administrators can manage the creation and approval of tuition " +
            "waivers for graduate students in real time using Business Process Technology.",
          image: GTWCoverImage,
          skills: [
            "BPT (Workflow)",
            "Business Systems Analysis",
            "CI/CD",
            "Outsystems",
          ],
        },
        {
          title: "KSU Workflow Management",
          description:
            "KSU Workflow Management is a complete workflow management tool that allows for tracking of submissions across all applications, configuration of workflow " +
            "steps, management of approval chains, proxy assignment, and more.",
          image: KSUWFCoverImage,
          skills: [
            "BPT (Workflow)",
            "SQL",
            "Outsystems",
            "Component-Based Development",
          ],
        },
        {
          title: "PayOnline",
          description:
            "PayOnline is the online payment system for Kent State University. It is utilized by students, authorized parents/guardians of students, and vendors. If a bill is paid " +
            "online at KSU, PayOnline is the system that is used.",
          image: PayOnlineCoverImage,
          skills: ["ASP.NET Web", "C#", "Responsive", "SSMS"],
        },
        {
          title: "Manage My Program",
          description:
            "Manage My Program is the application students use to manage Majors, Minors, and Certificates at Kent State University. Students can see approved changes to their program in real-time. To date, over 30,000 " +
            "students have made changes to their program using MMP.",
          image: MMPCoverImage,
          skills: ["SQL", "Outsystems", "BPT (Workflow)", "CI/CD", "Business Systems Analysis"],
        },
      ],
    };
  },
};
</script>

<style>
</style>
