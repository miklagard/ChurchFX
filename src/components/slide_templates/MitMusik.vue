<template>
  <section>
    <div>
      <div v-for="(text, index) in top" v-bind:key="index">
        {{ text }}
      </div>
    </div>

    <div>
      <div v-for="(text, index) in below" v-bind:key="index">
        {{ text }}
      </div>
    </div>
  </section>
</template>

<script>
import Reveal from 'reveal'

export default {
  name: "MitMuzik",
  props: ['top', 'below'],
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
  .present {
    font-variant: small-caps !important;
  }
</style>