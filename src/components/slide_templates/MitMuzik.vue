<template>
  <section>
    <div>
      mit<br />
      Pfarrer Dr. Ulrich Schöntube
    </div>

    <div>
      Musik:<br />
      Kreiskantor Jörg Walter<br />
      Frohnauer Kantatenchor und Kantorei
    </div>
  </section>
</template>

<script>
import Reveal from 'reveal'

export default {
  name: "MitMuzik",
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