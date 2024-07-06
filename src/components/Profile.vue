<template>
    <Container>
      <div class="profile-container">
            <h1>USERBAR</h1>
            <h1>IMAGEGALERY</h1>
      </div>
    </Container>
  </template>
  
  <script setup>
  import Container from "./Container.vue";
  import Card from "./Card.vue";

  </script>
  
  <style scoped>
  .profile-container {
    display: flex;
    flex-direction: column;
    align-items: center;
    padding: 20px 0;
  }
  .post-image {
    width: 100%;
    max-width: 640px;
    height: auto;
    margin-bottom: 1em;
  }
  </style>
  