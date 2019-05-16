<template>

  <div class="admin-edit-post-page">
    
    <section class="update-form">

      <AdminFormPost :post="loadedPost" />
    
    </section>
    
  </div>

</template>


<script>

import AdminFormPost from '@/components/Admin/FormPost'

export default {

  layout : 'admin',

  components : {
    AdminFormPost
  },
  data(){
    return {
      loadedPost : {
        id : 6,
        author : "PC",
        title : "PC Post Title",
        thumbnailLink : "https://www.homage.sg/wp-content/uploads/2018/09/47724337_l-1080x675.jpg",
        content : "This is my awesome post content, very nice!"
      }
    }
  }
  
}

</script>


<style scoped>

.update-form {
  width : 90%;
  margin :  20px auto;
}

@media (min-width : 768px){
  .update-form {
    width : 500px;
  }
}

</style>
