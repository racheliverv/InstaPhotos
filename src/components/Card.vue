<template>
    <a-card hoverable style="width: 240px" class="card">
      <template #cover>
        <img alt="example" src="https://os.alipayobjects.com/rmsportal/QBnOOoLaAfKPirc.png" />
      </template>
      <a-card-meta :title="props.username">
        <template #description>{{ props.fullName }}</template>
      </a-card-meta>
    </a-card>
  </template>
<script setup>
import { defineProps } from 'vue';
const props = defineProps(['id','username','profilePicture','fullName'])
</script>
<style scoped>
    .card {
        margin-bottom: 20px;
    }
</style>