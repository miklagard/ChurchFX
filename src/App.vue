<template>
  <div class="reveal">
    <div class="reveal">
      <div class="slides">
        <component
          v-for="(slide, index) in slides"
          v-bind:key="'auto' + index"
          v-bind:is="slide.component"
          :top="slide.top"
          :below="slide.below"
        />
      </div>
    </div>
  </div>
</template>

<script>
import Cover from "@/components/slide_templates/Cover"
import MitMusik from "@/components/slide_templates/MitMusik"
import WochenSpruch from "@/components/slide_templates/WochenSpruch"
import Guest from "@/components/slide_templates/Guest"
import Psalmgebet from "@/components/slide_templates/Psalmgebet"
import Prayer from "@/components/slide_templates/Prayer"
import Empty from "@/components/slide_templates/Empty"
import "reveal/index.css"
import "reveal/theme/moon.css"
import slides_json from "@/data/slides.json"

export default {
  name: 'App',
  components: {
    Cover,
    MitMusik,
    WochenSpruch,
    Guest,
    Psalmgebet,
    Prayer,
    Empty
  },
  data() {
    return {
      slides: slides_json,
    }
  }
}
</script>

<style>
  @font-face {
    font-family: "Franklin";
    src:
     url(https://allfont.net/cache/fonts/franklin-gothic-medium-cond_b0474bd036470b94941f78e56ac37217.ttf)
     format("truetype");
  }

  body {
    background-color: #00ff00;
  }

  .reveal {
    color: white;
  }

  .present {
    font-family: Franklin;
    font-size: 44pt;
    text-shadow: 2px 2px 2px #666;
  }
</style>
