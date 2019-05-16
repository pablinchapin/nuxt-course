<template>

  <div class="single-post-page">
    <section class="post">
      <h1 class="post-title">{{ loadedPost.title }}</h1>
      <div class="post-details">
        <div class="post-detail">Last updated on {{ loadedPost.updatedDate }}</div>
        <div class="post-detail">Written by {{ loadedPost.author }}</div>
      </div>
      <p class="post-content">{{ loadedPost.content }}</p>
    </section>

    <section class="post-feedback">
      <p>Let me know what youy think about the post, send an email to <a href="mailto:pablinchapin@gmail.com">Admin PC</a></p>
    </section>
  </div>
  
</template>

<script>
export default {

  asyncData(context, callback){
    setTimeout(() => {
      callback(null, {
        loadedPost : {
          id:4,
          thumbnail:"https://www.homage.sg/wp-content/uploads/2018/09/47724337_l-1080x675.jpg",
          title:"Title 4 (ID: "+ context.route.params.id +")",
          textPreview:"Text preview 4",
          author : "Don PC",
          updatedDate : new Date(),
          content : "Some dummy text ..., Some dummy text ..., Some dummy text ..., Some dummy text ..., Some dummy text ..."
        }
      })
    },1000)
  }
  
}
</script>

<style scoped>

.single-post-page {
  padding: 30px;
  text-align: center;
  box-sizing: border-box;
}

.post {
  width: 100%;
}

@media (min-width: 768px) {
  .post {
    width: 600px;
    margin: auto;
  }
}

.post-title {
  margin: 0;
}

.post-details {
  padding: 10px;
  box-sizing: border-box;
  border-bottom: 3px solid #ccc;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
}

@media (min-width: 768px) {
  .post-details {
    flex-direction: row;
  }
}

.post-detail {
  color: rgb(88, 88, 88);
  margin: 0 10px;
}

.post-feedback a {
  color: red;
  text-decoration: none;
}

.post-feedback a:hover,
.post-feedback a:active {
  color: salmon;
}

</style>
