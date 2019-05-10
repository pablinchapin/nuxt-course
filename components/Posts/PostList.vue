<template>

  <section class="posts-list">
    <PostPreview 
      :id="1"
      thumbnail="https://www.homage.sg/wp-content/uploads/2018/09/47724337_l-1080x675.jpg"
      title="Title 1"
      textPreview="Text preview 1"
    />

    <PostPreview 
      :id="2"
      thumbnail="https://www.homage.sg/wp-content/uploads/2018/09/47724337_l-1080x675.jpg"
      title="Title 2"
      textPreview="Text preview 2"
    />

    <PostPreview 
      :id="3"
      thumbnail="https://www.homage.sg/wp-content/uploads/2018/09/47724337_l-1080x675.jpg"
      title="Title 3"
      textPreview="Text preview 3"
    />
  </section>
  
</template>


<script>

import PostPreview from '@/components/Posts/PostPreview'

export default {

  components : {
    PostPreview
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
