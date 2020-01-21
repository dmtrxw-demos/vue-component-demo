<template>
  <div class="container">
    <Navbar />
    <div class="row mt-4">
      <div class="col-md-6">
        <AddArticleForm @article-form-submitted="saveArticle" />
      </div>
      <div class="col-md-6">
        <ArticleList :articles="articles" />
      </div>
    </div>
  </div>
</template>

<script>
import Navbar from '@/components/Navbar.vue';
import AddArticleForm from '@/components/AddArticleForm.vue';
import ArticleList from '@/components/ArticleList.vue';

export default {
  components: {
    Navbar,
    AddArticleForm,
    ArticleList,
  },
  data() {
    return {
      articles: [
        {
          id: 1,
          title: 'Foo',
          content: 'fooooo',
        },
        {
          id: 2,
          title: 'Bar',
          content: 'barrrrr',
        },
      ],
    };
  },
  methods: {
    saveArticle(payload) {
      this.articles.push(payload);
    },
  },
};
</script>
