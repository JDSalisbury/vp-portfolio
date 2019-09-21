<template>
  <div>
    <p class="desc">{{description}}</p>
    <p class="tools">{{tools}}</p>
  </div>
</template>

<script>
export default {
  props: ["description", "tools"]
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
</style>