<template>
  <p>
    <img :src="image" alt="" />
  </p>
</template>

<script>
export default {
  props: ["image"]
};
</script>

<style scoped>
p {
  display: flex;
  justify-content: center;
}
</style>
