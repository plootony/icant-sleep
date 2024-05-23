<template>
  <div class="animation">
    <div class="animation__media">
      <video autoplay muted loop>
        <source src="../assets/focus.mp4" type="video/mp4">
      </video>
    </div>

  </div>
  <div class="player">
    <h1 class="player__title">Focus</h1>
    <h2 class="player__subtitle">Evening Energy Fade</h2>
  </div>

  <div class="controls">
    <button
        v-for="icon in modes"
        :class="['btn btn--player']">
      <svg class="icon">
        <use :xlink:href="`/src/assets/sprite.svg#SVG-${icon.id}`"></use>
      </svg>
    </button>
  </div>
</template>

<script setup>
import {ref} from "vue";
const modes = ref([
  {
    id: 1,
    name: "Waves",
    description: "Calm and rhythmic waves",
    effect: 'waves',
    sound: 'waves'
  },
  {
    id: 2,
    name: "Book",
    description: "Knowledge and relaxation",
    effect: 'book',
    sound: 'book'
  },
  {
    id: 3,
    name: "Meditation",
    description: "Deep meditation aid",
    effect: 'meditation',
    sound: 'meditation'
  },
  {
    id: 4,
    name: "Yin Yang",
    description: "Balance and harmony",
    effect: 'yin_yang',
    sound: 'yin_yang'
  },
  {
    id: 5,
    name: "Palm Tree",
    description: "Tropical relaxation",
    effect: 'palm_tree',
    sound: 'palm_tree'
  },
  {
    id: 6,
    name: "Snowflake",
    description: "Cool and refreshing",
    effect: 'snowflake',
    sound: 'snowflake'
  },
  {
    id: 7,
    name: "Rain",
    description: "Soothing rain sounds",
    effect: 'rain',
    sound: 'rain'
  },
  {
    id: 8,
    name: "Molecules",
    description: "Scientific and calming",
    effect: 'molecules',
    sound: 'molecules'
  },
  {
    id: 9,
    name: "Moon",
    description: "Peaceful night ambiance",
    effect: 'moon',
    sound: 'moon'
  },
  {
    id: 10,
    name: "Stars",
    description: "Starry night sky",
    effect: 'stars',
    sound: 'stars'
  },
  {
    id: 11,
    name: "Grid",
    description: "Structured and organized",
    effect: 'grid',
    sound: 'grid'
  }
]);

</script>