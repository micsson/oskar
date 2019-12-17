<template>
  <Layout>
    <Post :post="$page.post">
      <header class="mb-4">
        <h1 class="text-break" v-html="$page.post.title" />
      </header>
      <template v-if="$page.post.tags.length">
        <h2 class="font-family-sans-serif h4">Tags:</h2>
        <ul class="list-inline">
          <li class="list-inline-item" v-for="tag in $page.post.tags" :key="tag.id">
            <b-button
              class="mb-2"
              variant="primary"
              size="sm"
              :to="tag.path"
            >{{ tag.title }} ({{ tag.count }})</b-button>
          </li>
        </ul>

        <g-link to="/" class="text-dark">
          <h2>Home</h2>
        </g-link>
      </template>
    </Post>
  </Layout>
</template>

<page-query>
query Post($path: String!) {
  post: wordPressPost(path: $path) {
    title
    date
    content
    featuredMedia {
      sourceUrl
      altText
      mediaDetails {
        width
      }
    }
    categories {
      id
      title
      path
    }
    tags {
      id
      title
      path
      count
    }
    author {
      name
      path
    }
  }
}
</page-query>

<script>
import Post from "~/components/Post.vue";
export default {
  components: {
    Post
  },
  metaInfo() {
    return {
      title: this.$page.post.title
    };
  }
};
</script>

<style>
p {
  display: none;
}

.meta-data {
  margin-top: 1.5rem;
}

</style>