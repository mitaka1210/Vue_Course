<template>

  <div class="app">
    <post-form  @create="createPost"/>
    <post-list :posts="posts"/>
  </div>

</template>

<script>
import PostForm from "@/components/PostForm";
import PostList from "@/components/PostList";
export default {
  components: {
    PostForm, PostList
  },
  data() {
    return {
      posts: [
        {id: 1, title: 'javaScript', body: 'Documentations 1'},
        {id: 2, title: 'javaScript', body: 'Documentations 2'},
        {id: 3, title: 'javaScript', body: 'Documentations 3'},
        {id: 4, title: 'javaScript', body: 'Documentations 4'}
      ],
      title: '',
      body: ''
    }
  },

  methods: {
    createPost(post) {
      this.posts.push(post);
      console.log(post);
    }
  }
}


</script>

<style>

  *{
     margin: 0;
    padding: 0;
    box-sizing: border-box;
  }
  .post{
    border: 1px solid red;
    padding: 1em;
    margin: 1em
  }

  input{
    width: 100%;
    border: 1px solid teal;
    padding: 10px 15px;
    margin-top:  15px;
  }

  .app{
    padding: 20px
  }

  form{
    display: flex;
    flex-direction: column;
  }


</style>