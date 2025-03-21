<template>
  <div id="app">
    <h1>Herbal Flashcards 🌿</h1>
    <div class="flashcards">
      <Flashcard v-for="(herb, index) in herbs" :key="index" :herb="herb" />
    </div>
  </div>
</template>

<script>
import Flashcard from "./components/FlashCard.vue";

export default {
  components: { Flashcard },
  data() {
    return {
      herbs: [
        {
          name: "ฟ้าทะลายโจร",
          image: "/img/ฟ้าทะลายโจร.jpg",
          uses: "Helps with colds, flu, and fever",
          partsUsed: "Leaves and stems",
        },
        {
          name: "ขมิ้นชัน",
          image: "/img/ขมิ้นชัน.jpg",
          uses: "Aids digestion and has anti-inflammatory properties",
          partsUsed: "Rhizome",
        },
      ],
    };
  },
};
</script>

<style>
#app {
  text-align: center;
  font-family: Arial, sans-serif;
}
.flashcards {
  display: flex;
  justify-content: center;
  gap: 20px;
  flex-wrap: wrap;
}
</style>
