<template>
  <section>
    <div class="rect">
      {{ title }}
    </div>

    <div>
      {{ psalm }}
    </div>
    <div>
      {{ eg }}
    </div>
  </section>
</template>

<script>
import Reveal from "reveal";

export default {
  name: "Psalmgebet",
  props: [
    'title',
    'psalm',
    'eg'
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
  .rect {
    border: 7px solid #ffffff;
    font-variant: small-caps !important;
  }
</style>