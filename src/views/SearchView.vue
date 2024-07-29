<template>
    <div>
        <h1>Search Page ({{ category }})</h1>
    </div>
</template>

<script setup>
import { computed } from 'vue';
import { useRoute } from 'vue-router';

const route = useRoute();
const categort = computed(() => route.params.category || 'all');
</script>