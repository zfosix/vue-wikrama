<template>
     <div class="blog">
          <h3> Blog</h3>

          <div class="row-blog">
               <Blog></Blog>
          </div>
          <div class="read-more">
               <a href="">Lihat lebih banyak</a>
          </div>
     </div>
</template>
<script>
import '@/assets/blog.css';
import Blog from '@/components/Blog/Card.vue';
export default {
     components: {
          Blog
     }
}
</script>

<style>
.blog h3
{
     margin: auto;
     font-family: "Poppins", sans-serif;
     font-weight: 900;
     font-size: 48px;
     line-height: 70px;
     color: #042181;
     margin-bottom: 15px;
     text-align: center;
}
</style>
