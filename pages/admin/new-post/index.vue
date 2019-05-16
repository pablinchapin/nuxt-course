<template>

  <div class="admin-new-post-page">
    
    <section class="new-post">

      <AdminFormPost />

    </section>
    
  </div>

</template>


<script>

import AdminFormPost from '@/components/Admin/FormPost'

export default {

  layout : 'admin',

  components : {
    AdminFormPost
  }
  
}

</script>


<style scoped>

.new-post {
  width : 90%;
  margin : 20px auto;
}

@media (min-width : 768px){
  .new-post {
    width : 500px;
  }
}

</style>
