<template>
  <div class="admin-post-page">
    <div class="update-form">
      <AdminPostForm :post="loadedPost" />
    </div>
  </div>
</template>

<script>
import AdminPostForm from "@/components/Admin/AdminPostForm";
export default {  
  name: 'AdminPostIdPage',
  layout: 'admin',
  components: {
    AdminPostForm
  },
  data() {
      return{
          loadedPost: {
              author: 'Gabriel',
              title: 'My awesome Post',
              content: 'Super amazing, thanks for that!',
              thumbnailLink: 'https://images.pexels.com/photos/546819/pexels-photo-546819.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=750&w=1260'
          }
      }
  }
};
</script>

<style scoped>
.update-form {
    width: 90%;
    margin: 20px auto;
}

@media(min-width: 768px) {
    .update-form {
        width: 500px;
    }
}
</style>