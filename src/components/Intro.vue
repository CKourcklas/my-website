<template>
  <div
    id="intro"
    class="flex flex-col md:flex-row justify-center items-center md:h-screen text-white introBackground pt-8 md:pt-0"
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
      <div class="md:text-xl mt-2">Specializing in ASP.NET, Outsystems, SQL, and Business Systems Analysis</div>
      <div class="px-8 md:px-0 mt-4 md:mt-0 flex flex-col md:flex-row md:justify-start md:mt-5">
        <div class="text-center flex">
          <a
            href="https://resume.io/r/GjepeXQ8c"
            target="_blank"
            class="button buttonMain w-full"
          >Resume</a>
        </div>
        <div class="text-center flex md:ml-6 mt-4 md:mt-0">
          <a
            href="https://www.linkedin.com/in/cory-kourcklas-6264451aa/"
            target="_blank"
            class="button buttonSecondary w-full"
          >LinkedIn</a>
        </div>
        <div class="text-center flex md:ml-6 mt-4 md:mt-0">
          <a
            href="mailto:ckourcklas@gmail.com"
            target="_blank"
            class="button buttonSecondary w-full"
          >Email</a>
        </div>
        <div class="text-center flex md:ml-6 mt-4 md:mt-0">
          <a
            href="https://github.com/CKourcklas/"
            target="_blank"
            class="button buttonSecondary w-full"
          >Github</a>
        </div>
      </div>
      <div class="mt-8" style="border: 2px solid #ed8936; border-radius: 5px;"></div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Intro",
  components: {}
};
</script>

<style scoped>
.introBackground {
  background: linear-gradient(to bottom right, #00206c 0%, #004cb8 100%);
}

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
