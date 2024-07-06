<template>
  <Container>
    <div class="profile-container">
      <UserBar
        :username="'laithharb'"
        :userinfo="{ posts: 4, followers: 4, following: 342 }"
      />
      <div class="container-posts">
     <ImageGallery :posts="[{
        id:1,
        image: 'https://pics.craiyon.com/2023-05-31/220e4c73f6674d46a84840ebde9f9bc8.webp'
     }]"/>
     <ImageGallery :posts="[{
        id:1,
        image: 'https://pics.craiyon.com/2023-05-31/220e4c73f6674d46a84840ebde9f9bc8.webp'
     }]"/>
     </div>
    </div>
  </Container>
</template>

<script setup>
import Container from "./Container.vue";
import UserBar from "./UserBar.vue";
import ImageGallery from "./ImageGallery.vue";
</script>

<style scoped>
.profile-container {
  display: flex;
    flex-direction: column;
    align-items: baseline;
    padding: 20px 0;
    margin: 10px 70px;
}
.post-image {
  width: 100%;
  max-width: 640px;
  height: auto;
  margin-bottom: 1em;
}
.container-posts {
  display: flex;
}
</style>
