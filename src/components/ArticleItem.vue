<template>
  <div class="card">
    <div class="card-body">
      <h5 class="card-title">{{ article.title }}</h5>
      <div class="card-text">{{ article.content }}</div>
    </div>
  </div>
</template>

<script>
export default {
  props: ['article'],
};
</script>
