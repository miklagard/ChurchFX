<template>
  <section>
  </section>
</template>

<script>
import Reveal from "reveal";

export default {
  name: "Empty",
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