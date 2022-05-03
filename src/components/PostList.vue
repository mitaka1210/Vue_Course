<template>
  <div>
    <h3> List Items</h3>
    <post-items v-for="post in posts" :post="post" />
  </div>
</template>

<script>
import PostItems from "./PostItems";
export default {
  name: "PostList.vue",
  components: {PostItems},
  props:{
    posts:{
      type: Array,
      required: true
    }
  }
}
</script>


<style scoped>

*{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
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

.bnt{
  align-self: center;
  margin-top: 15px;
  padding: 10px 15px;

}
</style>