<template>
  <section>
    <div class="rect">
      WOCHENSPRUCH
    </div>

    <div>
      Also hat Gott die Welt geliebt, dass er seinen
      eingeborenen Sohn gab, damit alle die an ihn glauben
      nicht verloren werden, sondern das ewige Leben haben.
    </div>
  </section>
</template>

<script>
import Reveal from 'reveal'

export default {
  name: "WochenSpruch",
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
  }
</style>