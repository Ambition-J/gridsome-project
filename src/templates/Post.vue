<template>
  <div>
    <div>{{ $page.post.title }}</div>
    <div>{{ $page.post.content }}</div>
  </div>
</template>
<page-query>
query ($id: ID!) {
  post (id: $id) {
    id
    title
    content
  }
}
</page-query>
<script>
export default {
  metaInfo() {
    return {
      title: this.$page.post.title,
    };
  },
};
</script>

<style>
</style>