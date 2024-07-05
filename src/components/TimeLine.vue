<template>
    <Container>
        <div class="timeline-container">
            <Card />
            <Card />
            <Card />
        </div>
    </Container>
</template>

<script setup>
    import Container from './Container.vue'
    import Card from './Card.vue'
</script>

<style scoped>
.timeline-container {
    display: flex;
    flex-direction: column;
    align-items: center;
    padding: 20px 0;
}
</style>