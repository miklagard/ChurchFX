<template>
  <div class="reveal">
    <div class="reveal">
      <div class="slides">
        <section data-auto-animate>
          Willkommen zu<br />
          unserem Gottesdienst<br />
          Ostersonntag<br />
          4. April 2021
        </section>
        <section data-auto-animate>Vertical Slide 1</section>
        <section>Vertical Slide 2</section>
      </div>
    </div>
  </div>
</template>

<script>
import Reveal from 'reveal'

export default {
  name: "Cover",
  mounted() {
    Reveal.initialize({

    })
  }
}
</script>

<style scoped>
  .present {
    font-family: Franklin;
    font-size: 44px;
    font-variant: small-caps;
    text-shadow: 4px 4px 4px #aaa;

  }
</style>