<template>
    <div class="flashcard" @click="flipCard">
      <div v-if="!flipped">
        <h2>{{ herb.name }}</h2>
        <img :src="herb.image" alt="Herb Image" />
      </div>
      <div v-else>
        <p><strong>Uses:</strong> {{ herb.uses }}</p>
        <p><strong>Parts Used:</strong> {{ herb.partsUsed }}</p>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    props: ["herb"],
    data() {
      return { flipped: false };
    },
    methods: {
      flipCard() {
        this.flipped = !this.flipped;
      },
    },
  };
  </script>
  
  <style scoped>
  .flashcard {
    width: 300px;
    height: 200px;
    border: 1px solid #ccc;
    padding: 10px;
    text-align: center;
    cursor: pointer;
    background: white;
    box-shadow: 2px 2px 10px rgba(0, 0, 0, 0.1);
  }
  img {
    width: 100px;
    height: 100px;
    object-fit: cover;
  }
  </style>
  