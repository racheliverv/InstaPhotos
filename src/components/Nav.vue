<template>
  <a-layout-header class="layout-header">
    <Container>
      <div class="nav-container">
        <div class="right-content">
          <RouterLink to="/">Instagram</RouterLink>
          <a-input-search
            v-model:value="searchUsername"
            placeholder="username..."
            style="width: 200px"
            @search="onSearch"
          />
        </div>
        <div class="left-content">
          <a-button type="primary">SignUp</a-button>
          <a-button type="primary">Login</a-button>
        </div>
      </div>
    </Container>
  </a-layout-header>
</template>

<script setup>
import { RouterLink } from "vue-router";
import Container from "./Container.vue";
import { ref } from "vue";

const searchUsername = ref("");

const onSearch = () => {};
</script>

<style lang="css" scoped>
.nav-container {
  display: flex;
  justify-content: space-between;
}
.right-content {
  display: flex;
  align-items: center;
}
.right-content a {
  margin-right: 10px;
}

.left-content button {
  margin-left: 10px;
}
</style>
