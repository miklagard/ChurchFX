<template>
  <section>
    <div class="rect">
      {{ guest }}
    </div>

    <div class="title">
      {{ title }}
    </div>
  </section>
</template>

<script>
export default {
  name: "Guest",
  props: [
    'guest',
    'title'
  ]
}
</script>

<style scoped>
  .rect {
    border: 7px solid #ffffff;
  }
</style>