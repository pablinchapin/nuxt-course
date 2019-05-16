<template>

  <section class="posts-list">
    <PostPreview 
      v-for="post in posts"
      :key="post.id"

      :id="post.id"
      :isAdmin="isAdmin"
      :thumbnail="post.thumbnail"
      :title="post.title"
      :textPreview="post.textPreview"
    />

  </section>
  
</template>


<script>

import PostPreview from '@/components/Posts/PostPreview'

export default {

  components : {
    PostPreview
  },
  props: {
    isAdmin : {
      type : Boolean,
      default : false
    },
    posts : {
      type : Array,
      required : true
    }
  }
  
}
</script>


<style>

  .posts-list {
    display: flex;
    padding: 20px;
    box-sizing: border-box;
    flex-wrap: wrap;
    align-items: center;
    justify-content: center;
  }

</style>
