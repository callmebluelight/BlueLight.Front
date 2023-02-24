<template>
    <h1>this is {{ $route.params.id }} page</h1>
    <ArticleDetail />
</template>
<script setup>
import ArticleDetail from '../components/ArticleDetail.vue'
</script>