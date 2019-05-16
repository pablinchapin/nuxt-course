<template>
  <div class="home-page">
    
    <section class="intro">
      <h1>Get the latest tech news!</h1>
    </section>

    <PostList :posts="this.loadedPosts" />
  
  </div>
</template>

<script>

import PostList from '@/components/Posts/PostList'
import { Promise } from 'q';

export default {
  components : {
    PostList
  },
  data(){
    /*
    return {
      loadedPosts : []      
    }
    */
    
  },
  asyncData(context, callback){

    console.warn('asyncData executed!')

    setTimeout(() => {

      callback(null,  
      {
        loadedPosts : 
      [
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


    },1000)

    
  },
  created(){
    /*
    setTimeout(() => {

      this.loadedPosts = 
      [
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



    },1000)
    */
  }

  
}
</script>


<style scoped>

.intro {
  height: 300px;
  position: relative;
  padding: 30px;
  box-sizing: border-box;
  background-position: center;
  background-image: url('~assets/images/tech-header-01.jpg');
  background-size: cover;
}

.intro h1 {
  position: absolute;
  top: 10%;
  left: 5%;
  width: 90%;
  font-size: 1.5rem;
  color: black;
  background-color: rgb(211, 211, 211);
  padding: 10px;
  border-radius: 10px;
  box-shadow: 3px 3px 3px black;
  box-sizing: border-box;
  border: 1px solid black;
}

@media (min-width: 768px) {
  .intro h1 {
    font-size: 2rem;
  }
}


/*
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
*/
</style>
