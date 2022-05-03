<template>
  <slot>
    <button class="bnt">Create</button>
  </slot>
</template>

<script>
export default {
  name: "MyButton.vue"
}
</script>

<style scoped>
.bnt{
  align-self: end;
  margin-top: 15px;
  padding: 10px 15px;

}
</style>