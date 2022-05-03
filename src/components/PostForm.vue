<template>
  <div class="app">
    <form @submit.prevent>
      <input
          type="text"
          v-model="post.title"
          placeholder="Name">
      <input
          type="text"
          placeholder="Description"
          v-model="post.body" >
      <my-button @click="createPost"/>
    </form>
  </div>
</template>

<script>

export default {
  name: "PostForm.vue"
  data() {
    return {
      post:{
        title: '',
        body: ''
      }
    }
  },
  methods: {
    createPost() {
      this.post.id = Date.now();
      this.$emit('create', this.post)
      this.post = {
        title: '',
        body: ''
      }
    },
  }
}
</script>

<style scoped>

</style>