<template>
  <div
    id="intro"
    class="flex flex-col md:flex-row justify-center items-center h-screen text-white introBackground"
  >
    <div class="border-0 md:border-8 md:relative border-orange-500 positionDiv">
      <img
        src="../assets/img/Sample.jpg"
        alt="Portrait"
        class="border-2 border-white md:absolute top"
        style="top: 29px; left: 33px;"
      />
    </div>
    <div class="mt-6 text-center md:text-left md:relative md:ml-20 md:mt-0">
      <div class="text-4xl text-7xl">
        <span class="font-bold">Cory</span>
        <span class="m-2" style="color: #ed8936">Kourcklas</span>
      </div>
      <div class="md:text-3xl mt-4">Full Stack Developer with 4+ years experience</div>
      <div class="md:text-xl mt-2">Specializing in ASP.NET, Outsystems, SQL, and front end design</div>
      <div class="flex justify-center md:justify-start mt-6">
        <a href="https://www.google.com" target="-_blank" class="button buttonMain">Resume</a>
        <a
          href="https://www.linkedin.com"
          target="-_blank"
          class="button buttonSecondary ml-6"
        >LinkedIn</a>
      </div>
      <div class="mt-8" style="border: 2px solid #ed8936; border-radius: 5px;"></div>
    </div>
    <buttonLinksComp />
  </div>
</template>

<script>
import ButtonLinksComp from "./ButtonLinks.vue";

export default {
  name: "Intro",
  components: {
    ButtonLinksComp
  }
};
</script>

<style scoped>
@media (min-width: 768px) {
  .positionDiv {
    height: 25rem;
    width: 14rem;
  }
}

@media (min-width: 768px) {
  .text-7xl {
    font-size: 5rem;
  }
}

.introBackground {
  background: linear-gradient(to bottom right, #00206c 0%, #004cb8 100%);
}

.button {
  background-color: transparent;
  border-radius: 0.25rem;
  padding: 0.75rem 2rem 0.75rem 2rem;
  font-weight: 600;
  --text-opacity: 1;
}

.buttonMain {
  border: 2px solid #ed8936;
  color: #ed8936;
}

.buttonMain:hover {
  background-color: #ed8936;
  color: white;
  border: 2px solid white;
}

.buttonSecondary {
  border: 2px solid white;
  color: white;
}

.buttonSecondary:hover {
  background-color: white;
  color: #ed8936;
  border: 2px solid #ed8936;
}
</style>
