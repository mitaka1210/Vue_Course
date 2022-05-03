<template>
  <div class="post">
    <div>
      <div> <strong>Name</strong> {{post.title}}</div>
      <div> <strong>Description</strong> {{post.body}}</div>
    </div>
    <div class="post__bnt">
      <button>remove</button>
    </div>

  </div>

</template>

<script>
export default {
  name: "PostItems.vue",
  props: {
    post: {
      type: Object,
      required: true
    }
  }
}
</script>

<style scoped>
.post{
  border: 1px solid red;
  padding: 1em;
  margin: 1em;
  display: flex;
  justify-content: space-between;

}
.post__bnt{
  display: flex;
  align-items: center;
  justify-content: center;
}
</style>