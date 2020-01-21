<template>
  <div class="card">
    <div class="card-body">
      <form @submit.prevent="handleFormSubmit">
        <div class="form-group">
          <label for="title">Title</label>
          <input
            class="form-control"
            type="text"
            id="title"
            v-model="title"
            autocomplete="off"
          />
        </div>
        <div class="form-group">
          <label for="content">Content</label>
          <input
            class="form-control"
            type="text"
            id="content"
            v-model="content"
            autocomplete="off"
          />
        </div>
        <div class="form-group">
          <button class="btn btn-dark">Submit</button>
        </div>
      </form>
    </div>
  </div>
</template>

<script>
export default {
  name: 'AddArticleForm',
  data() {
    return {
      title: '',
      content: '',
    };
  },
  methods: {
    handleFormSubmit() {
      this.$emit('article-form-submitted', { title: this.title, content: this.content });
    },
  },
};
</script>
