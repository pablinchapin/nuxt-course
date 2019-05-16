<template>
  <div class="admin-page">

    <section class="new-post">
      <AppButton @click="$router.push('/admin/new-post/')"> Create Post </AppButton>
    </section>

    <section class="existing-posts">
      <h1>Existing Posts</h1>
      
      <PostList :posts="loadedPosts" isAdmin/>
    </section>

  </div>
  
  
</template>


<script>

import PostList from '@/components/Posts/PostList'
import AppButton from '@/components/UI/AppButton'

export default {

  layout : 'admin',

  components : {
    PostList,
    AppButton
  },
  asyncData(context, callback){

    console.warn('asyncData executed!')
    
    setTimeout(()  => {

      callback(null, {
        
        loadedPosts : [
          {
            id:1,
            isAdmin:"isAdmin",
            thumbnail:"https://www.homage.sg/wp-content/uploads/2018/09/47724337_l-1080x675.jpg",
            title:"Title 1",
            textPreview:"Text preview 1",
          },
          {
            id:2,
            isAdmin:"isAdmin",
            thumbnail:"https://www.homage.sg/wp-content/uploads/2018/09/47724337_l-1080x675.jpg",
            title:"Title 2",
            textPreview:"Text preview 3",
          },
          {
            id:3,
            isAdmin:"isAdmin",
            thumbnail:"https://www.homage.sg/wp-content/uploads/2018/09/47724337_l-1080x675.jpg",
            title:"Title 3",
            textPreview:"Text preview 3",
          }
        ]
      })
      



      

    }, 1000)

  }


  
}
</script>

<style scoped>

.admin-page {
  padding: 20px;
}

.new-post {
  text-align: center;
  border-bottom: 2px solid #cccccc;
  padding-bottom: 10px;
}

.existing-posts h1 {
  text-align: center;

}

</style>
