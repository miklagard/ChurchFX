<template>
  <div class="reveal">
    <div class="reveal">
      <div class="slides">
        <component v-bind:is="cover" />
        <component v-bind:is="mit_muzik" />
        <component v-bind:is="wochen_spruch" />
        <component v-bind:is="guest"
            guest="Sebastian Huck"
            title="Prädikant"
        />
        <component v-bind:is="guest"
            guest="Dr. Ulrich Schöntube"
            title="Gemeindepfarrer"
        />
        <component v-bind:is="psamlgebet"
          title="Psalmgebet im Wechsel"
          psalm="Psalm 69"
          eg="EG 731"
        />

        <component v-bind:is="prayer"
          v-for="(pray, index) in prays"
          v-bind:key="index"
          :top="pray.top"
          :below="pray.below"
        />

        <component v-bind:is="empty" />

      </div>
    </div>
  </div>
</template>

<script>
import Cover from "@/components/slide_templates/Cover"
import MitMuzik from "@/components/slide_templates/MitMuzik"
import WochenSpruch from "@/components/slide_templates/WochenSpruch"
import Guest from "@/components/slide_templates/Guest"
import Psalmgebet from "@/components/slide_templates/Psalmgebet"
import Prayer from "@/components/slide_templates/Prayer"
import Empty from "@/components/slide_templates/Empty"
import "reveal/index.css"
import "reveal/theme/moon.css"

export default {
  name: 'App',
  components: {
    Cover,
    MitMuzik,
    WochenSpruch,
    Guest,
    Psalmgebet,
    Prayer,
    Empty
  },
  data() {
    return {
      cover: Cover,
      mit_muzik: MitMuzik,
      wochen_spruch: WochenSpruch,
      guest: Guest,
      psamlgebet: Psalmgebet,
      prayer: Prayer,
      empty: Empty,
      prays: [
        {
          top: [
            'Gott, hilf mir!',
            'Denn das Wasser geht mir bis an die Kehle.'
          ],
          below: [
            'Ich versinke in tiefem Schlamm, wo kein Grund ist;',
            'ich bin in tiefe Wasser geraten, und die Flut will mich ersäufen.'
          ]
        },
        {
          top: [
            'Ich habe mich müde geschrien,',
            'mein Hals ist heiser.'
          ],
          below: [
            'Meine Augen sind trübe geworden,',
            'weil ich so lange harren muss auf meinen Gott.'
          ]
        },
        {
          top: [
            'Ich aber bete zu dir, Herr, zur Zeit der Gnade;',
            'Gott, nach deiner großen Güte erhöre mich mit deiner treuen Hilfe.'
          ],
          below: [
            'Errette mich aus dem Schlamm,',
            'dass ich nicht versinke,'
          ]
        },
        {
          top: [
            'dass ich errettet werde vor denen, die mich hassen,',
            'und aus den tiefen Wassern;'
          ],
          below: [
            'dass mich die Flut nicht ersäufe und die Tiefe nicht verschlinge',
            'und das Loch des Brunnens sich nicht über mir schließe.'
          ]
        },
        {
          top: [
            'Erhöre mich, Herr, denn deine Güte ist tröstlich;',
            'wende dich zu mir nach deiner großen Barmherzigkeit'
          ],
          below: [
            'und verbirg dein Angesicht nicht vor deinem Knechte,',
            'denn mir ist angst; erhöre mich eilends.'
          ]
        },
        {
          top: [
            'Nahe dich zu meiner Seele und erlöse sie,',
            'Gott, deine Hilfe schütze mich!'
          ],
          below: []
        },
      ]
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
