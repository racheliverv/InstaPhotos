<template>
  <Container>
    <div class="timeline-container">
      <div v-for="item in data" :key="item.id">
        <h2>Post ID: {{ item.id }}</h2>
        <div v-for="comment in item.comments.data" :key="comment.id">
          <Card
            :id="comment.from.id"
            :username="comment.from.username"
            :profilePicture="comment.from.profile_picture"
            :fullName="comment.from.full_name"
            :text="comment.text"
          />
        </div>
      </div>
    </div>
  </Container>
</template>

<script setup>
import Container from "./Container.vue";
import Card from "./Card.vue";
import instaData from "@/assets/instaData.json"; // Adjust the path as needed

import { ref } from "vue";

const data = ref(instaData.data);
</script>

<style scoped>
.timeline-container {
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
