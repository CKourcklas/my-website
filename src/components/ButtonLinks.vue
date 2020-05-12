<template>
  <div>
    <div v-bind:key="index" v-for="(buttonLink, index) in buttonLinks">{{buttonLink.name}}</div>
  </div>
</template>

<script>
export default {
  name: "ButtonLinksComp",
  components: {},
  data() {
    return {
      buttonLinks: [
        {
          name: "Resume",
          linkTo: "https://www.google.com"
        },
        {
          name: "linkedIn",
          linkTo: "https://www.linkedIn.com"
        },
        {
          name: "Email",
          linkTo: "mailto:ckourcklas@gmail.com"
        }
      ]
    };
  }
};
</script>

<style>
</style>