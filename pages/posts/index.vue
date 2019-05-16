<template>

  <div class="posts-page">

    <PostList :posts="loadedPosts"/>    
    
  </div>
  
</template>


<script>

import PostList from '@/components/Posts/PostList'

export default {

  components : {
    PostList
  },
  asyncData(context){


    return new Promise((resolve, reject) =>{

      setTimeout(()=> {
      resolve({

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

      
    })
    .then(data => {
      return data
    })
    .catch(error => {
      context.error(new Error())
    })
    //console.warn('asyncData executed!')
  },
  created(){
    this.$store.dispatch('setPosts', this.loadedPosts)
  }
  
}
</script>

<style scoped>

.posts-page {
  display: flex;
  justify-content: center;
  align-items: center;
}

</style>
