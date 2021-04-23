<template>
  <section>
    <div class="top">
      <div v-for="(text, index) in top" v-bind:key="index">
        {{text}}
      </div>
    </div>
    <div class="below">
      <div v-for="(text, index) in below" v-bind:key="index">
        {{text}}
      </div>
    </div>
  </section>
</template>

<script>
import Reveal from "reveal";

export default {
  name: "Prayer",
  props: [
    'top', 'below'
  ],
  mounted() {
    Reveal.initialize({
      transition: 'fade', // none/fade/slide/convex/concave/zoom
      transitionSpeed: 'slow', // default/fast/slow
      controls: false,
      hideAddressBar: true,
    })
  }
}
</script>

<style scoped>

</style>