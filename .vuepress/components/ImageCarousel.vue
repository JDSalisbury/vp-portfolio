<template>
  <div style="width: 400px; display:block; margin:0 auto;">
    <carousel :per-page="1" :center-mode="true">
      <slide>
        <img width="90%" src="/images/pp1.png">
      </slide>
      <slide>
        <img width="90%" src="/images/pp2.png">
      </slide>
      <slide>
        <img width="90%" src="/images/pp3.png">
      </slide>
      <slide>
        <img width="90%" src="/images/pp4.png">
      </slide>
    </carousel>
  </div>
</template>

<script>
import { Carousel, Slide } from "vue-carousel";

export default {
  components: {
    Carousel,
    Slide
  }
  /*
  mounted () {
    import('vue-carousel').then(module => {
      // Vue.use(module);
      // Vue.component('carousel', module.Carousel);
    });
  }
   */
};
</script>