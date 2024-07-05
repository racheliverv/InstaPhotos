<template>
    <div>
      <a-button type="primary" @click="showModal">{{ title }}</a-button>
      <a-modal v-model:visible="open" :title="title" @ok="handleOk">
        <a-input v-if="!isLogin" v-model:value="value" placeholder="Username" />
        <a-input v-model:value="value" placeholder="Email" />
        <a-input v-model:value="value" placeholder="Password" />
      </a-modal>
    </div>
  </template>
  
  <script setup>
  import { ref, defineProps } from 'vue';
  
  const props = defineProps(['isLogin'])
  const open = ref(false);
  const title = props.isLogin ? 'Login' : 'Sign Up';
  const showModal = () => {
    open.value = true;
  };
  
  const handleOk = () => {
    open.value = false;
  };
  </script>


<style scoped>
  input {
    margin-top: 5px;
  }
</style>
  