<template>
  <div>
    <ArticleItem
      v-for="article in articles"
      :key="article.id"
      class="mb-4"
      v-bind:article="article"
    />
  </div>
</template>

<script>
import ArticleItem from '@/components/ArticleItem.vue';

export default {
  props: ['articles'],
  components: {
    ArticleItem,
  },
};
</script>
