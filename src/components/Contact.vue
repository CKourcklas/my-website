<template>
  <div id="contact" class="px-8 md:px-0 py-10 md:py-24 text-center text-white introBackground">
    <div>
      <span class="text-2xl md:text-5xl">Looking for a developer?</span>
    </div>
    <div class="flex flex-col md:flex-row justify-center mt-6">
      <a href="https://resume.io/r/GjepeXQ8c" target="_blank" class="button buttonMain">Resume</a>
      <a
        href="https://www.linkedin.com/in/cory-kourcklas-6264451aa/"
        target="_blank"
        class="button buttonSecondary mt-4 md:mt-0 md:ml-6"
        style="flex: 0 0 50px;"
      >LinkedIn</a>
      <a
        href="mailto:ckourcklas@gmail.com"
        target="_blank"
        class="button buttonSecondary mt-4 md:mt-0 md:ml-6"
      >Email</a>
    </div>
  </div>
</template>

<script>
export default {
  name: "Contact",
  components: {}
};
</script>

<style scoped>
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
