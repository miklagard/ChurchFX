<template>
  <Cover />
</template>

<script>
import Cover from "@/components/slide_templates/Cover"
import "reveal/index.css"
import "reveal/theme/moon.css"

export default {
  name: 'App',
  components: {
    Cover
  }
}
</script>

<style>
@font-face {
  font-family: "Franklin";
  src:
   url(https://allfont.net/cache/fonts/franklin-gothic-heavy_4d13be3d7e0bde3cf8be37610dc835bf.ttf) format("truetype");
}

body {
  background-color: #00ff00;
}

.reveal {
  color: white;
}

</style>
