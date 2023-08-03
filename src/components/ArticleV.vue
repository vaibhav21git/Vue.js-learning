<template>
  <div>
    <h2>Article Component</h2>
    <h2>{{ title }}</h2>
    <h2>Likes - {{ likes }}</h2>
    <h2>isPublished - {{ isPublished ? "Yes" : "No" }}</h2>
  </div>
</template>

<script>
export default {
  name: "ArticleV",
  props: {
    title: {
      type: String,
      required: true,
      default: "Article default title",
    },
    likes: Number,
    isPublished: Boolean,
  },
};
</script>

<style lang="scss" scoped></style>
