<template>
    <div class="userbar-container">
        <div class="top-content">
            <a-typography-title :level="2">{{ props.username }}</a-typography-title>
        </div>
        <div class="bottom-content">
            <a-typography-title :level="5">{{ props.userinfo.posts }} posts</a-typography-title>
            <a-typography-title :level="5">{{props.userinfo.followers}} followers</a-typography-title>
            <a-typography-title :level="5">{{props.userinfo.following}} following</a-typography-title>
        </div>
    </div>
</template>

<script setup>
    import {defineProps} from 'vue';
    const props = defineProps(['username', 'userinfo']);
</script>

<style scoped>
.userbar-container{
    display: table-column;
    padding-bottom: 75px;
}
.bottom-content {
    display: flex;
    align-items: center;
    justify-content: space-around;
}

.bottom-content h5{
    margin: 0;
    margin-right: 30px;
}
</style>