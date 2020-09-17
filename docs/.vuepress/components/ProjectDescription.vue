<template>
  <div>
    <div class="img-div">
      <img
        class="p-img"
        v-if="src_image"
        :src="$withBase(`/images/${src_image}`)"
      />
    </div>
    <p class="desc">{{ description }}</p>
    <p class="tools">{{ tools }}</p>
  </div>
</template>

<script>
export default {
  props: ['description', 'tools', 'src_image']
};
</script>

<style>
.desc {
  width: 100%;
}
.tools {
  font-size: small;
  font-style: italic;
}
.img-div {
  display: flex;
  justify-content: center;
}
.p-img {
  max-width: 80%;
  height: auto;
  border: 1px solid #ddd;
  border-radius: 4px;
  padding: 5px;
}
</style>
