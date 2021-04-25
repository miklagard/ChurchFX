<template>
  <section>
    <div class="rect">
      <div v-for="(text, index) in top" v-bind:key="index">
        {{ text }}
      </div>
    </div>

    <div class="title">
      <div v-for="(text, index) in below" v-bind:key="index">
        {{ text }}
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "Guest",
  props: [
    'top',
    'below'
  ]
}
</script>

<style scoped>
  .rect {
    border: 7px solid #ffffff;
  }
</style>