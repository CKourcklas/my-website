<template>
  <div class="px-4">
    <div
      class="h-full w-full md:relative md:border-8 hidden md:block"
      :style="[(index % 2 !== 0) ? {'border-color': '#004cb8'} : {'border-color': '#ed8936'}]"
      style="height: 550px; width: 750px;"
    >
      <a>
        <img
          v-bind:src="work.slides[slideIndex]"
          :alt="work.imageDesc"
          class="md:absolute md:shadow-2xl m-border-black cursor-pointer"
          :style="[(index % 2 !== 0) ? {'left': '40px'} : {'right': '40px'}]"
          style="transition: all 150ms ease-in-out 0s; width:100%;
   height:550px;
   object-fit:cover;
   object-position:50% 50%;"
          @click="updateSlideshow(work.slidesLength)"
        />
      </a>
    </div>
    <div class="md:w-16"></div>
    <div class="mt-6 mb-6 md:mt-0 pl-4 pr-4 md:p-0 max-w-xl">
      <div class="text-lg md:text-4xl font-bold">{{work.title}}</div>
      <div class="mt-4">{{work.description}}</div>
      <div class="mt-6 md:mt-12 uppercase font-bold md:text-lg">Skills Used</div>
      <div class="flex flex-wrap justify-evenly mt-4">
        <div
          v-bind:key="skill.index"
          v-for="skill in work.skills"
          class="font-bold text-lg bg-gray-300 rounded-lg mt-5 p-4 text-center"
          style="min-width: 6rem;"
        >{{skill}}</div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      slideIndex: 0,
    };
  },
  name: "work",
  props: ["work", "index"],
  methods: {
    outputClickedWork(work) {
      this.$emit("show-slides", work);
    },
    updateSlideshow(length) {
      if (this.slideIndex < length) {
        this.slideIndex = this.slideIndex + 1;
      } else {
        this.slideIndex = 0;
      }
    },
  },
};
</script>

<style scoped>
@media (min-width: 768px) {
  .m-size-550 {
    height: 550px;
    width: 998px;
  }
}

@media (min-width: 768px) {
  .m-display {
    display: block;
  }
}

@media (max-width: 400){
  .s-hide{
    display: none;
  }
}

@media (min-width: 768px) {
  .m-border-black {
    border: 1px solid black;
  }
}

img:hover {
  bottom: 40px;
}

img {
  bottom: 25px;
}
</style>